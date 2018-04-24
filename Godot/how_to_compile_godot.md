# How to compile Godot

## Windows

### Install scons

- Install Python 2.7
- Run `pip install scons`
- Run `pip install pywin32`, this is for multi-thread compilation

### Grab Godot engine source code

- `git clone https://github.com/godotengine/godot.git`

### Compile

- Open **x86 Native Tools Command Prompt for VS 2017**
- Run `scons p=windows -j8`, j is the number
- Generating VS project, Run `scons p=windows vsproj=yes`

Done.
