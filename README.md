# sungurerdim.github.io

CV site: `index.html` (EN) and `tr/index.html` (TR). The text-based PDFs in `cv/` are printed from these pages with headless Chrome; regenerate both after any content change (Git Bash, from the repository root):

```sh
C="/c/Program Files/Google/Chrome/Application/chrome.exe"; "$C" --headless=new --disable-gpu --no-pdf-header-footer --virtual-time-budget=10000 --print-to-pdf="$PWD/cv/Sungur_Zahid_Erdim_CV_EN.pdf" "file://$(pwd -W)/index.html" && "$C" --headless=new --disable-gpu --no-pdf-header-footer --virtual-time-budget=10000 --print-to-pdf="$PWD/cv/Sungur_Zahid_Erdim_CV_TR.pdf" "file://$(pwd -W)/tr/index.html"
```

Check after regenerating: two A4 pages each, selectable text (no images), headings Summary / Results / Technical Skills / Experience / Education / Certifications / Languages.
