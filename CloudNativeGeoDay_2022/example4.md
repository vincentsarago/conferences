
### COG - mix blocksize - 42.6Mb

    $ rio cogeo info https://sentinel-cogs.s3.us-west-2.amazonaws.com/sentinel-s2-l2a-cogs/2020/S2A_34SGA_20200318_0_L2A/B05.tif

    Driver: GTiff
    File: https://sentinel-cogs.s3.us-west-2.amazonaws.com/sentinel-s2-l2a-cogs/2020/S2A_34SGA_20200318_0_L2A/B05.tif
    COG: True
    Compression: DEFLATE
    ColorSpace: None

    Profile
        Width:            5490
        Height:           5490
        Bands:            1
        Tiled:            True
        Dtype:            uint16
        NoData:           0.0
        Alpha Band:       False
        Internal Mask:    False
        Interleave:       BAND
        ColorMap:         False
        ColorInterp:      ('gray',)
        Scales:           (1.0,)
        Offsets:          (0.0,)

    Geo
        Crs:              EPSG:32634
        Origin:           (699960.0, 3600000.0)
        Resolution:       (20.0, -20.0)
        BoundingBox:      (699960.0, 3490200.0, 809760.0, 3600000.0)
        MinZoom:          8
        MaxZoom:          13

    Image Metadata
        AREA_OR_POINT: Area
        OVR_RESAMPLING_ALG: AVERAGE

    Image Structure
        COMPRESSION: DEFLATE
        INTERLEAVE: BAND

    Band 1
        ColorInterp: gray

    IFD
        Id      Size           BlockSize     Decimation
        0       5490x5490      512x512       0
        1       2745x2745      256x256       2
        2       1373x1373      256x256       4
        3       687x687        256x256       8
        4       344x344        256x256       16


### COG - 256 blocks - 42.4 Mb

    $ rio cogeo create B05.tif B05_256.tif -p deflate --blocksize 256 --overview-blocksize 256


### COG - 512 blocks - 42.9 Mb

    $ rio cogeo create B05.tif B05_512.tif -p deflate --blocksize 512 --overview-blocksize 512


### COG - 1024 blocks - 43.6 Mb

    $ rio cogeo create B05.tif B05_1024.tif -p deflate --blocksize 1024 --overview-blocksize 1024

### COG - 2048 blocks - 44 Mb

    $ rio cogeo create B05.tif B05_2048.tif -p deflate --blocksize 2048 --overview-blocksize 2048


### Bench

    $ tilebench profile http://0.0.0.0:8000/B05_256.tif --tile 11-1156-829 | jq
    {
        "LIST": {
            "count": 0
        },
        "HEAD": {
            "count": 1
        },
        "GET": {
            "count": 3,
            "bytes": 81920,
            "ranges": [
            "0-32767",
            "3424256-3457023",
            "4046848-4063231"
            ]
        },
        "Timing": 0.1592719554901123
    }

    $ tilebench profile http://0.0.0.0:8000/B05_512.tif --tile 11-1156-829 | jq
    {
        "LIST": {
            "count": 0
        },
        "HEAD": {
            "count": 1
        },
        "GET": {
            "count": 3,
            "bytes": 294912,
            "ranges": [
            "0-32767",
            "2883584-2965503",
            "4063232-4243455"
            ]
        },
        "Timing": 0.15716791152954102
    }

    $ tilebench profile http://0.0.0.0:8000/B05_1024.tif --tile 11-1156-829 | jq
    {
        "LIST": {
            "count": 0
        },
        "HEAD": {
            "count": 1
        },
        "GET": {
            "count": 2,
            "bytes": 278528,
            "ranges": [
            "0-32767",
            "2785280-3031039"
            ]
        },
        "Timing": 0.1520709991455078
    }

    $ tilebench profile http://0.0.0.0:8000/B05_2048.tif --tile 11-1156-829 | jq
    {
        "LIST": {
            "count": 0
        },
        "HEAD": {
            "count": 1
        },
        "GET": {
            "count": 2,
            "bytes": 4096000,
            "ranges": [
            "0-32767",
            "2244608-6307839"
            ]
        },
        "Timing": 0.17275595664978027
    }




### Web Optimized - 56.5Mb

    $ rio cogeo create B05.tif B05_web_256.tif -w --blocksize 256 --aligned-levels 5

    $ rio cogeo info B05_web_256.tif
    Driver: GTiff
    File: /Users/vincentsarago/Dev/CloudNativeDay/B05_web_256.tif
    COG: True
    Compression: DEFLATE
    ColorSpace: None

    Profile
        Width:            16384
        Height:           16384
        Bands:            1
        Tiled:            True
        Dtype:            uint16
        NoData:           0.0
        Alpha Band:       False
        Internal Mask:    False
        Interleave:       BAND
        ColorMap:         False
        ColorInterp:      ('gray',)
        Scales:           (1.0,)
        Offsets:          (0.0,)

    Geo
        Crs:              EPSG:3857
        Origin:           (2504688.542848654, 3913575.8482010234)
        Resolution:       (19.109257071294063, -19.109257071294063)
        BoundingBox:      (2504688.542848654, 3600489.7803449417, 2817774.610704736, 3913575.8482010234)
        MinZoom:          7
        MaxZoom:          13

    Image Metadata
        AREA_OR_POINT: Area
        OVR_RESAMPLING_ALG: NEAREST

    Image Structure
        COMPRESSION: DEFLATE
        INTERLEAVE: BAND
        LAYOUT: COG

    Tiling Scheme
        ALIGNED_LEVELS: 5
        NAME: WEBMERCATORQUAD
        ZOOM_LEVEL: 13

    Band 1
        ColorInterp: gray

    IFD
        Id      Size           BlockSize     Decimation
        0       16384x16384    256x256       0
        1       8192x8192      256x256       2
        2       4096x4096      256x256       4
        3       2048x2048      256x256       8
        4       1024x1024      256x256       16
        5       512x512        256x256       32
        6       256x256        256x256       64


