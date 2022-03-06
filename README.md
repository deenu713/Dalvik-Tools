# Dalvik-BundleTool without installing java

# No need to install Java 
# Commands :- 

In Termux 

pkg install aapt2 

download the dalvik bundletool.zip

# For base.zip to aab

dalvikvm -Xcompiler-option --compiler-filter=speed -Xmx256m -cp path to bundletool bundletool-1.8.2.zip com.android.tools.build.bundletool.BundleToolMain build-bundle --modules=/path to zip Base-Module.zip --output=/path to aab Base-Module.aab

# For aab to apks

dalvikvm -Xcompiler-option --compiler-filter=speed -Xmx256m -cp /path to bundletool bundletool-1.8.2.zip com.android.tools.build.bundletool.BundleToolMain build-apks --bundle=/path to aab /Base-Module.aab --output=/path to apks Base-Module.apks --mode=universal --aapt2=aapt2 
