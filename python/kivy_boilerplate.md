# kivy boilerplate code

```python
from kivy.app import App
from kivy.uix.screenmanager import ScreenManager, Screen
from kivy.lang import Builder

Builder.load_file('frontend.kv')  


class FirstScreen(Screen):
	pass


class RootWidget(ScreenManager):
    pass


class MainApp(App):
    def build(self):
        return RootWidget()


if __name__ == "__main__":  
    MainApp().run()
```