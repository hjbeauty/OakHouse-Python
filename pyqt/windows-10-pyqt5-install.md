# Windows 10 PyQt5 install

{% hint style="info" %}
PyQt : Qt의 레이이웃에 Python의 코드를 연결하여 GUI FrameWork
{% endhint %}

{% hint style="info" %}
설치

* \(venv\) D:\works\pyqt\_test&gt;pip install PyQt5 
{% endhint %}

![](../.gitbook/assets/image%20%28299%29.png)

또는 직접 다운로드

{% embed url="https://www.riverbankcomputing.com/software/pyqt/download" %}

{% hint style="info" %}
테스트 
{% endhint %}

```python
import  sys
from PyQt5.QtWidgets import QApplication, QWidget

class MyApp(QWidget) :
    def __init__(self):
        super().__init__()
        self.initUtil()

    def initUtil(self):
        self.setWindowTitle('Ss')
        self.move(300,300)
        self.resize(400,200)
        self.show()


# Press the green button in the gutter to run the script.
if __name__ == '__main__':
    app = QApplication(sys.argv)
    ex = MyApp()
    sys.exit(app.exec_())
```

![](../.gitbook/assets/image%20%28300%29.png)



