# Setup

## References 

- [hypr/wiki doc](https://wiki.hypr.land/Hypr-Ecosystem/hyprcursor/)
- [hypr/making doc](https://github.com/hyprwm/hyprcursor/blob/main/docs/MAKING_THEMES.md)
- [arch/wiki doc](https://wiki.archlinux.org/title/Cursor_themes#XDG_specification)

- [windows to x11 cursor](https://github.com/quantum5/win2xcur)

- [x11 conventions](https://www.freedesktop.org/wiki/Specifications/cursor-spec/) `you can also use cursor view to map the correct aliases`

## Deps

- xcur2png

## Steps

You can use existing cursors as a reference for the folder structure, because you will have to create the `[theme/cursors]` and `[theme/index.theme]`

```fish
# Install win2xcur
uv pip install win2xcur

# Convert Windows cursor to X11
uv run win2xcur input/*.ani -o output/

# Extract x11 cursor
hyprcursor-util --extract . 

# Create boilerplate with extracted cursor
cd [extracted-folder]
hyprcursor-util --create . 
```
```
