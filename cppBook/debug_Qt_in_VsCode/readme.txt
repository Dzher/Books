Debugging with Visual Studio Code

Just download qt5.natvis.xml, or using this link: https://raw.github.com/aambrosano/qt-natvis/master/qt5.natvis.xml

Update your launch configurations(Ctrl+Shift+P, and type "preference settings") on Visual Studio Code to include this line:

"visualizerFile": "/path/to/qt5.natvis.xml"

You can find more about how to use Visual Studio Code for Qt development on KDAB's website: https://kdab.com/


Using Qt with a custom namespace name

If you built or are using a custom Qt version with a customized namespace, just replace ##NAMESPACE## with the namespace name in qt5.natvis.orig.xml with your favourite string manipulation tool.

For example using sed:
sed s/##NAMESPACE##/mynamespace/ qt5.natvis.orig.xml > qt5.natvis.mynamespace.xml