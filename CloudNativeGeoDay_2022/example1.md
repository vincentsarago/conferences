
## https://storage.googleapis.com/cfo-public/vegetation/California-Vegetation-CanopyBaseHeight-2016-Summer-00010m.tif


### Info

    rio cogeo info https://storage.googleapis.com/cfo-public/vegetation/California-Vegetation-CanopyBaseHeight-2016-Summer-00010m.tif

    Driver: GTiff
    File: https://storage.googleapis.com/cfo-public/vegetation/California-Vegetation-CanopyBaseHeight-2016-Summer-00010m.tif
    COG: True
    Compression: LZW
    ColorSpace: None

    Profile
        Width:            94338
        Height:           103969
        Bands:            1
        Tiled:            True
        Dtype:            int16
        NoData:           -9999.0
        Alpha Band:       False
        Internal Mask:    False
        Interleave:       BAND
        ColorMap:         False
        ColorInterp:      ('gray',)
        Scales:           (1.0,)
        Offsets:          (0.0,)

    Geo
        Crs:              EPSG:32610
        Origin:           (374310.0, 4653580.0)
        Resolution:       (10.0, -10.0)
        BoundingBox:      (374310.0, 3613890.0, 1317690.0, 4653580.0)
        MinZoom:          5
        MaxZoom:          14

    Image Metadata
        AREA_OR_POINT: Area
        Band_1: Band 1

    Image Structure
        COMPRESSION: LZW
        INTERLEAVE: BAND
        LAYOUT: COG
        PREDICTOR: 2

    Band 1
        ColorInterp: gray
        Metadata:
            STATISTICS_MAXIMUM: 29
            STATISTICS_MEAN: 0.89117618817673
            STATISTICS_MINIMUM: 0
            STATISTICS_STDDEV: 1.3718205083877
            STATISTICS_VALID_PERCENT: 42.08

    IFD
        Id      Size           BlockSize     Decimation
        0       94338x103969   512x512       0
        1       47169x51985    512x512       2
        2       23585x25993    512x512       4
        3       11793x12997    512x512       8
        4       5897x6499      512x512       16
        5       2949x3250      512x512       32
        6       1475x1625      512x512       64
        7       738x813        512x512       128
        8       369x407        512x512       256
        9       185x204        512x512       510


## Viz


    $ rio viz https://storage.googleapis.com/cfo-public/vegetation/California-Vegetation-CanopyBaseHeight-2016-Summer-00010m.tif

    curl http://127.0.0.1:8080/statistics\?categorical\=True | jq

    {
        "1": {
            "min": 0,
            "max": 8,
            "mean": 0.8981392324644126,
            "count": 402952,
            "sum": 361907,
            "std": 1.205316859234669,
            "median": 0,
            "majority": 0,
            "minority": 8,
            "unique": 9,
            "histogram": [
            [
                219131,
                76375,
                57670,
                33162,
                12774,
                3447,
                379,
                11,
                3
            ],
            [
                0,
                1,
                2,
                3,
                4,
                5,
                6,
                7,
                8
            ]
            ],
            "valid_percent": 42.31,
            "masked_pixels": 549368,
            "valid_pixels": 402952,
            "percentile_2": 0,
            "percentile_98": 4
        }
    }


## Bench


    $ tilebench viz https://storage.googleapis.com/cfo-public/vegetation/California-Vegetation-CanopyBaseHeight-2016-Summer-00010m.tif

