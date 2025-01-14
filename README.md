# dotbim-ifc

## Purpose

Converts IFC to dotbim.

## Prerequirements

You need to install dotbimpy library (version >= 0.1.0) (https://github.com/paireks/dotbimpy):

```cmd
pip install dotbimpy
```

You also need IfcOpenShell 0.7.0 installed. You can get it from here: https://github.com/IfcOpenBot/IfcOpenShell/commit/883b8a523c63027f2f6c91650385d47edba5521b#commitcomment-65879927
Place this folder in your project where this script is located.

## How to use it

Going to ...

```python
ifc = ifcopenshell.open("foobar.ifc")
ifc2dotbim = Ifc2Dotbim(ifc)
ifc2dotbim.execute()
ifc2dotbim.write("foobar.bim")
```

Coming from ...

```python
dotbim = dotbimpy.File.read("foobar.bim")
dotbim2ifc = Dotbim2Ifc(dotbim)
dotbim2ifc.execute()
dotbim2ifc.write("foobar.ifc")
```

## Alternative solution for .ifc -> .bim

Another approach could be to use another open-source project, which is https://3dviewer.net/.

On this website you can easily drag and drop .ifc file and export it to .bim.

The conversion in the viewer has been made with the help of web-ifc ifc.js (https://github.com/IFCjs/web-ifc).

This Python script however use ifcopenshell (https://github.com/IfcOpenShell/IfcOpenShell) for conversion.

Depending on a various factors such as your .ifc file, or how well each library can handle it, you can find different results.
