# addpythontags

This is a shell script that will add python tags to your code using ctags. I made it because everything I could find online either didn't work right, didn't install correctly, or some other such bullshit. I didn't want to install some overly-bloated plugin to do simple tab jumping. Ctags has support for python code, but I couldn't figure out how to get it to recurse through library files, so I was always limited to the code that was in my working directory tree. I used vim because I'm on an old computer and something like vscode takes too much system resources. I just wanted tags that actually jumped to the fucking definition of shit I was trying to navigate. Maybe there's an easier (better) way to do this and someone will tell me that I'm an idiot, but, if there is, I couldn't figure it out.

This works. just make sure that execution is enabled (`chmod +x addpythontags`) and then put it in some directory on your `$PATH` (probably either `/usr/bin/` or `~/.local/bin`).

To run it, simply go to your working directory, and run `addpythontags`. A `tags` file will be generated in your directory and then when you open the file in vim you can jump to a definition with `Ctrl+]` and then jump back to where you were with `Ctrl+t`.

There is some stuff that is like a binary file or whatever the hell, and those don't work. Apparently they're called "shared objects" (they end with `.so`). Some notable examples that I came across are `time` and `binascii`. I don't know if there is any possible way to access definitions in these files. Obviously they can be accessed to some degree, since python is calling them, but I got too frustrated to figure it out.

Anyways, I hope this script helps someone. It took me an entire weekend to make it.
