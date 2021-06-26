# [Module] DCM to IMG

### Function

- Change DICOM file to Image file (*.dcm → *.png, *.bmp, *.jpg, etc)

### Version

- python: 3.7
- matplotlib: 3.4.2
- numpy: 1.21.0
- pydicom: 2.1.2

### Use

- python dcm2img -i test.dcm -o test -t .png -wc 450 -ww 500

### Arguments

- **-i, --input**: input_file_path (or name)
- **-o, --output**: output_file_path (or name)
- **-t, --type**: file_extension_type
- **-wc, --window-center**: WC(Window Center)
- **-ww, --window-width**: WW(Window Width)

### Rules

- input_file_path argument(-i, --input) **must required.**
- If output_file_path argument(-o, --output) include file type, file_type argument(-t, --type) **will be ignored**.

    ex) python dcm2img -i test.dcm -o test.png -t .jpg → (result) test.png

- If you do not enter wc & ww arguments(-wc, -ww), it will **get from DICOM metadata**.