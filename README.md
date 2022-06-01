# pyqt-loading-progressbar
PyQt progress bar used for loading

## Requirements
* PyQt5 >= 5.8

## Setup
`python -m pip install pyqt-loading-progressbar`

## Example
Code Sample
```python
from PyQt5.QtWidgets import QMainWindow, QApplication, QVBoxLayout, QLabel, QWidget
from pyqt_loading_progressbar.loadingProgressBar import LoadingProgressBar


class MainWindow(QMainWindow):
    def __init__(self):
        super().__init__()
        self.__initUi()

    def __initUi(self):
        bar = LoadingProgressBar()
        lay = QVBoxLayout()
        lay.addWidget(QLabel('Loading...'))
        lay.addWidget(bar)
        mainWidget = QWidget()
        mainWidget.setLayout(lay)
        self.setCentralWidget(mainWidget)


if __name__ == "__main__":
    import sys

    app = QApplication(sys.argv)
    w = MainWindow()
    w.show()
    app.exec_()
```

Result

https://user-images.githubusercontent.com/55078043/171343160-88a38bbf-cc7a-4d83-b2b1-66d7291999ef.mp4
