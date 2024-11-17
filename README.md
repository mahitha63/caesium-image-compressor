## Caesium Image Compressor  [![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/Lymphatus)

[![Build](https://github.com/Lymphatus/caesium-image-compressor/actions/workflows/build-qt.yml/badge.svg)](https://github.com/Lymphatus/caesium-image-compressor/actions/workflows/build-qt.yml)

Try it directly on browser at [caesium.app](https://caesium.app)
- Readme file done by 21MIC0033 Bandaru Mahitha
###### v2.8.2

![image](https://github.com/user-attachments/assets/e24b3cfb-986e-41e6-9e86-667673f1d5a7)


---------

### What is it for

Caesium is an image compression software that helps you store, send and share digital pictures, supporting JPG, PNG and WebP formats.You can quickly reduce the file size (and resolution, if you want) by preserving the overall quality of the image.
### Caesium Image Compressor: A free and open-source image compressor that can reduce image file sizes by up to 90% without losing original quality. It offers features like batch processing, drag-and-drop functionality, customizable compression levels, and support for various file formats and languages.


### Supported Platforms

- **Windows**: 10 (build 1809 or later) (use old version v1.x for Windows 7 or
  8 - [link](https://www.fosshub.com/Caesium-Image-Compressor-old.html))
- **MacOS**: 10.15+
- **Linux**: tested on Ubuntu 22.04 and Manjaro

Note: only 64bit versions are supported

### Installation

Head to the [releases' page](https://github.com/Lymphatus/caesium-image-compressor/releases) for the available
downloads.

- **Windows**: installer and portable versions are available
- **MacOS**: DMG package
- **Linux**: compile the source code yourself, or download binary
  from [third-party build](https://github.com/larygwil/caesium-image-compressor/releases)

Note that the main branch can contain unstable code. If you want to build on a stable version, use a tagged version.

### Troubleshooting and/or feature request

Please open an [issue](https://github.com/Lymphatus/caesium-image-compressor/issues).

### Build from source

##### Requirements

- [Rust](https://www.rust-lang.org/tools/install): required to
  compile [libcaesium](https://github.com/Lymphatus/libcaesium). Make sure you have `cargo` executable on you `$PATH`
- [Qt6 SDK](https://www.qt.io/download/): binaries are built on 6.8.0 (open source)
- [libssh](https://www.libssh.org/): macOS only
- [Sparkle](https://sparkle-project.org/): macOS only. Only version 1.27.1 is supported.

#### Build

##### Step 0 (for macOS Only)

You need to set up Sparkle in order to compile the project

```
brew install --cask https://raw.githubusercontent.com/Homebrew/homebrew-cask/c6dfe6baf1639998ba1707f68668cf8fa97bac9d/Casks/sparkle.rb
sudo cp -R /usr/local/Caskroom/sparkle/1.27.1/Sparkle.framework /Library/Frameworks/Sparkle.framework
```

##### Step 1

You need to configure CMake first and the command is slightly different for all the platforms:
Change the path in variables with the correct directories of the requirements.

###### for Windows only

```
cmake -B build_dir -DCMAKE_PREFIX_PATH=/path/to/Qt/version -G "MinGW Makefiles"
```

##### Step 2

Then you can build with

```
cmake --build build_dir --config Release --target caesium_image_compressor
```

##### Step 3
Once the build is done, you can upload any image of your interest through the upload option and can adjust the quality, size, etc.. parameters. You can also choose whether you need a lossy or lossless compression. You have to select a location on your pc where the output should be stored.
- The image I need to compress is : ![image](https://github.com/user-attachments/assets/b9d1bbca-3f46-4c94-a246-66fed3e0e3aa)

- In my assignment, I chose for lossless compression with optimization level to 6 (max).
![image](https://github.com/user-attachments/assets/7748570a-8bad-450d-849d-e06a65538d5a)

##### Step 4
Once you select compress, you can see that the compressed image is saved in the given output location. 
![image](https://github.com/user-attachments/assets/149ec49c-b81e-4737-aead-ea8c6b5ac13b)

The image before compression :
![image](https://github.com/user-attachments/assets/d57e5415-e679-4f11-a8e8-9a7785a1f2ff)

The image after compression :
![image](https://github.com/user-attachments/assets/8d1fcac5-b2fe-470d-8f0a-892fb61557cc)

----- end of the readme file -------
