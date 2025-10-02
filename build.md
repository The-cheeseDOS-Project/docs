# Build and Run

Here's how to get cheeseDOS up and running on your computer or on QEMU

> [!WARNING]
> On real hardware, cheeseDOS has direct access to low-level components and **may cause irreversible damage**. While no such incidents have occurred, this is experimental software—**USE AT YOUR OWN RISK!**

> [!IMPORTANT]
> Only 1.44MB floppy's with a CHS capable BIOS have a chance of working, use QEMU if you don't have those.

> [!NOTE]
> If you have any problems, please open an issue, you **WILL** get help!

## Prerequisites
You will need a working GNU toolchain, `git`, and standard UNIX utilities.

## Cloning
You will need to get the latest version of cheeseDOS: 
```sh
git clone --depth=1 https://github.com/The-cheeseDOS-Project/cheeseDOS.git && \
cd cheeseDOS
```

## Configuring
You need to configure cheeseDOS before compiling, you can just run:

```sh
./configure.sh
```

by itself and that will use the default options (`i386`, `32`, `s`, `cheeseDOS.img`, `sudo`.), but you can use diffrent options then the default one.

### Configure flags

| Flag          | Purpose                          | Applicable values               |
|---------------|----------------------------------|---------------------------------|
| `--march=`    | Target CPU architecture          | Varies                          |
| `--bits=`     | Target bit width                 | `32`, `64`                      |
| `--optimize=` | Optimization level               | `0`, `1`, `2`, `3`, `s`, `fast` |
| `--floppy=`   | Target filename                  | Any                             |
| `--sudo=`     | **S**uper**U**ser **DO** command | `sudo`, `doas`                  |

## Compilation
Then you want to compile cheeseDOS:
```sh
./build.sh
```

## Testing
After that'sone, you now have cheeseDOS compiled, if you just want to use it in QEMU, you can run:
```sh
./build.sh run
```

## Writing
Page moved over [here](./writing.md).

## Miscellaneous
For all build.sh arguments, refer to [this](./build.sh-arguments.md).
