# lv-bin-7zip

lv-bin-7zip is an lv-bin package that allows compression and extraction of an archive; it also provides the ability to create "installers" that can self extract and run a specific application (e.g. setup.exe or run.bat).

## Installation

The lv-bin-7zip library requires lv-bin be installed via vipm or copied into <user.lib>/antonio-alexander/lv-bin and copying lv-bin-7zip into <user.lib>/antonio-alexander/lv-bin-7zip. The vipm installation is ideal in that it manages a lot of the extra effort for you (especially the palettes and paths).

This package was built specifically with **v9.20** of the 7zip libraries, to download the binaries navigate to [https://www.7-zip.org/download.html](https://www.7-zip.org/download.html) and download "7-Zip Extra: standalone console version, 7z DLL, Plugin for Far Manager". This will give you all the files utilized by lv-bin-7zip.

## Description

As described above, 7zip provides you with an api that allows interaction with archives (extraction and compression) as well as creating installers.

* api v1 (v1.lvlib)
  * compress.vi: this vi can be used to create an archive providing the "source" folder to populate the archive as well as the archive name. It's as intelligent as the 7zip application, depending on the archive extension you give, it will create an archive with the appropriate extension (i.e. zip, 7z, tar, gz). If no archive is provided, it will prompt you to select a new or existing file. If a folder is given, it will add the contents of the folder.
  * extract.vi: this can be used to extract one or more files from an archive, it also has the ability to "preview" files that would be extracted from an archive rather than actually extract them.
  * make_installer.vi: this vi can be used with the given configuration to create a self-extracting installer, it can provide the executable to run and generate an exe.

## Example 01 - Compress

![v1.lvlib:examples/example_01_compress.vi](../../doc/lv-bin-7zip/v1_example_01_compress.png "Compress")

## Example 02 - Extract (Archive)

![v1.lvlib:examples/example_02_extract.vi](../../doc/lv-bin-7zip/v1_example_02_extract.png "Extract")

## Example 03 - Extract (Specific)

![v1.lvlib:examples/example_03_extract_specific.vi](../../doc/lv-bin-7zip/v1_example_03_extract_specific.png "Extract (Specific)")

## Example 04 - Make Installer

![v1.lvlib:examples/example_04_make_installer.vi](../../doc/lv-bin-7zip/v1_example_04_make_installer.png "Make Installer")
