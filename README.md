# pyqt-loading-progressbar
PyQt animated progress bar used for loading

There are two types of animation - dynamic, fade.

Animation is set to dynamic by default.

You can set it with `setAnimationType(type: str)`. You can give 'dynamic' or 'fade' to `type` argument.

## Requirements
* PyQt5 >= 5.8

## Setup
`python -m pip install pyqt-loading-progressbar`

## Example
### Code Sample
```python
from PyQt5.QtWidgets import QMainWindow, QApplication, QVBoxLayout, QLabel, QWidget
from pyqt_loading_progressbar.loadingProgressBar import LoadingProgressBar


class MainWindow(QMainWindow):
    def __init__(self):
        super().__init__()
        self.__initUi()

    def __initUi(self):
        bar = LoadingProgressBar()
        # bar.setAnimationType('fade') - if you want to set animation type to fade
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

### Result

#### Dynamic

https://user-images.githubusercontent.com/55078043/171343160-88a38bbf-cc7a-4d83-b2b1-66d7291999ef.mp4

#### Fade

https://user-images.githubusercontent.com/55078043/171527713-ef74326d-a84f-499f-a79f-1efc17e4ab76.mp4
