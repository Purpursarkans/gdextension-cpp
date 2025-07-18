# gdextension-cpp


folder look like:

root  \
|\
+-- demo(project folder, name can change in SCon file)\
|\
+-- [godot-cpp](https://github.com/godotengine/godot-cpp)\
|\
+--src/\****past file here***\*\
|\
+--Scon file

build

```
cd "gdextension_cpp/godot-cpp/"

"godot/bin/godot.linuxbsd.editor.double.x86_64.mono"  --dump-extension-api

scons platform=linux custom_api_file=extension_api.json arch=x86_64 precision=double module_mono_enabled=yes
scons platform=windows custom_api_file=extension_api.json arch=x86_64 precision=double module_mono_enabled=yes

cd "gdextension_cpp/"

scons platform=linux arch=x86_64 precision=double module_mono_enabled=yes
scons platform=linux arch=x86_64 precision=double module_mono_enabled=yes target=template_release

scons platform=windows arch=x86_64 precision=double module_mono_enabled=yes
scons platform=windows arch=x86_64 precision=double module_mono_enabled=yes target=template_release
```

https://docs.godotengine.org/en/stable/tutorials/scripting/gdextension/gdextension_cpp_example.html
