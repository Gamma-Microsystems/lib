# SiriusOS System Libraries

These are the core system libraries of SiriusOS. Where functionality isn't expected in the C standard library, these provide additional features that are shared by multiple SiriusOS applications.

## `sirius_auth`

Provides password validation and login helper methods. Exists primarily because `libc` doesn't have these things and there are multiple places where logins are checked (`login`, `glogin`, `sudo`, `gsudo`...).

## `sirius_button`

Renderer for button widgets. Not really a widget library at the moment.

## `sirius_confreader`

Implements a basic INI parser for use with configuration files.

## `sirius_decorations`

Client-side decoration library for the compositor. Supports pluggable decoration themes through additional libraries, which are named as `libsirius_decor-...`.

## `sirius_graphics`

General-purpose 2D drawing and pixel-pushing library. Provides sprite blitting, rotation, scaling, etc.

## `sirius_hashmap`

Generic hashmap implementation. Also used by the kernel.

## `sirius_iconcache`

Convenience library for loading icons at specific sizes.

## `sirius_inflate`

Decompression library for DEFLATE payloads.

## `sirius_jpeg`

Minimal, incomplete JPEG decoder. Mostly used for providing wallpapers. Doesn't support most JPEG features.

## `sirius_kbd`

Keyboard scancode parser.

## `sirius_list`

Generic expandable linked list implementation.

## `sirius_markup`

XML-like syntax parser.

## `sirius_menu`

Menu widget library. Used for the "Applications" menu, context menus, etc.

## `sirius_pex`

Userspace library for using the siriusOS "packetfs" subsystem, which provides packet-based IPC.

## `sirius_png`

Decoder for Portable Network Graphics images.

## `sirius_rline`

Rich line editor for terminal applications, with support for tab completion and syntax highlighting.

## `sirius_termemu`

Terminal ANSI escape processor.

## `sirius_text`

TrueType font parser and text renderer.

## `sirius_tree`

Generic tree implementation. Also used by the kernel.

## `sirius_yutani`

Compositor client library, used to build GUI applications.
