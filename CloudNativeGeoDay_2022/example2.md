
## https://globalnightlight.s3.amazonaws.com/201206/SVDNB_npp_d20120601_t0113490_e0119294_b03074_c20120601071930512114_noaa_ops.rade9.co.tif


### Info

    rio cogeo info https://globalnightlight.s3.amazonaws.com/201206/SVDNB_npp_d20120601_t0113490_e0119294_b03074_c20120601071930512114_noaa_ops.rade9.co.tif

    Driver: GTiff
    File: https://globalnightlight.s3.amazonaws.com/201206/SVDNB_npp_d20120601_t0113490_e0119294_b03074_c20120601071930512114_noaa_ops.rade9.co.tif
    COG: True
    Compression: LZW
    ColorSpace: None

    Profile
        Width:            13200
        Height:           6240
        Bands:            1
        Tiled:            True
        Dtype:            float32
        NoData:           None
        Alpha Band:       False
        Internal Mask:    False
        Interleave:       BAND
        ColorMap:         False
        ColorInterp:      ('gray',)
        Scales:           (1.0,)
        Offsets:          (0.0,)

    Geo
        Crs:              EPSG:4326
        Origin:           (-12.002083335, 64.002083335)
        Resolution:       (0.00416667, -0.00416667)
        BoundingBox:      (-12.002083335, 38.00206253499999, 42.997960664999994, 64.002083335)
        MinZoom:          2
        MaxZoom:          8

    Image Metadata
        AREA_OR_POINT: Area
        TIFFTAG_DATETIME: 2017:09:26 14:26:21
        TIFFTAG_DOCUMENTNAME: npp_d20120601_t0113490_e0119294_b03074/SVDNB_npp_d20120601_t0113490_e0119294_b03074_c20120601071930512114_noaa_ops.rade9.tif
        TIFFTAG_IMAGEDESCRIPTION: IDL TIFF file
        TIFFTAG_RESOLUTIONUNIT: 2 (pixels/inch)
        TIFFTAG_SOFTWARE: IDL 8.5.1, Exelis Visual Information Solutions, Inc., a subsidiary of Harris Corporation.
        TIFFTAG_XRESOLUTION: 100
        TIFFTAG_YRESOLUTION: 100

    Image Structure
        COMPRESSION: LZW
        INTERLEAVE: BAND

    Band 1
        ColorInterp: gray
        Metadata:
            STATISTICS_MAXIMUM: 1181207.875
            STATISTICS_MEAN: 7073.6160909262
            STATISTICS_MINIMUM: -999.29998779297
            STATISTICS_STDDEV: 33173.248131921
            STATISTICS_VALID_PERCENT: 100

    IFD
        Id      Size           BlockSize     Decimation
        0       13200x6240     256x256       0
        1       6600x3120      128x128       2
        2       3300x1560      128x128       4
        3       1650x780       128x128       8
        4       825x390        128x128       16
        5       413x195        128x128       32
        6       207x98         128x128       64


## Viz


    $ rio viz https://globalnightlight.s3.amazonaws.com/201206/SVDNB_npp_d20120601_t0113490_e0119294_b03074_c20120601071930512114_noaa_ops.rade9.co.tif
