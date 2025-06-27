# PDF OCR Excel 填表系统

这是一个使用 Flask 构建的简单网页应用，用于上传 PDF 文件并识别其中的中文内容，将识别结果填入提供的 Excel 模板中并生成新的表格下载。

## 安装依赖

```bash
pip install -r requirements.txt
```

本项目依赖 tesseract OCR，请确保系统已安装 `tesseract`，并且安装了中文语言包 `tesseract-ocr-chi-sim`。

Ubuntu 下可以使用：

```bash
sudo apt-get install tesseract-ocr tesseract-ocr-chi-sim
```

## 运行

```bash
python app.py
```

在浏览器访问 `http://localhost:5000`，上传待识别的 PDF 与 Excel 模板，即可获得填充后的表格文件。

## 说明

- 如果 PDF 为扫描件或图片，程序会自动使用 OCR 识别中文文字；
- 程序会根据关键字（如“姓名”、“身份证号”、“单位名称”）匹配相应内容，并填入 Excel 模板的指定单元格，可在 `app.py` 中调整 `MAPPING` 字典来自定义。 
