
## s3://naip-analytic/wa/2017/100cm/rgbir_cog/48117/m_4811762_se_11_1_20170723.tif


### Info

    AWS_REQUEST_PAYER=requester rio cogeo info s3://naip-analytic/wa/2017/100cm/rgbir_cog/48117/m_4811762_se_11_1_20170723.tif

    Driver: GTiff
    File: s3://naip-analytic/wa/2017/100cm/rgbir_cog/48117/m_4811762_se_11_1_20170723.tif
    COG: True
    Compression: DEFLATE
    ColorSpace: None

    Profile
        Width:            5306
        Height:           7586
        Bands:            4
        Tiled:            True
        Dtype:            uint8
        NoData:           None
        Alpha Band:       True
        Internal Mask:    False
        Interleave:       PIXEL
        ColorMap:         False
        ColorInterp:      ('red', 'green', 'blue', 'alpha')
        Scales:           (1.0, 1.0, 1.0, 1.0)
        Offsets:          (0.0, 0.0, 0.0, 0.0)

    Geo
        Crs:              EPSG:26911
        Origin:           (476378.0, 5323606.0)
        Resolution:       (1.0, -1.0)
        BoundingBox:      (476378.0, 5316020.0, 481684.0, 5323606.0)
        MinZoom:          12
        MaxZoom:          17

    Image Metadata
        AREA_OR_POINT: Area
        TIFFTAG_IMAGEDESCRIPTION: OrthoVista
        TIFFTAG_RESOLUTIONUNIT: 1 (unitless)
        TIFFTAG_SOFTWARE: Trimble Germany GmbH
        TIFFTAG_XRESOLUTION: 1
        TIFFTAG_YRESOLUTION: 1

    Image Structure
        COMPRESSION: DEFLATE
        INTERLEAVE: PIXEL

    Band 1
        ColorInterp: red

    Band 2
        ColorInterp: green

    Band 3
        ColorInterp: blue

    Band 4
        ColorInterp: alpha

    IFD
        Id      Size           BlockSize     Decimation
        0       5306x7586      512x512       0
        1       2653x3793      128x128       2
        2       1327x1897      128x128       4
        3       664x949        128x128       8
        4       332x475        128x128       16


## Viz

    $  AWS_REQUEST_PAYER=requester rio viz s3://naip-analytic/wa/2017/100cm/rgbir_cog/48117/m_4811762_se_11_1_20170723.tif
