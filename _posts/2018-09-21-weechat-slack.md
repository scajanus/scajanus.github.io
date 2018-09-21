I didn't use a computer for 16 months, and getting back into using one I did it super carefully. I chose to use OS X over Linux, didn't change a default setting or even a colorscheme on _anything_. I even run my `vim` without a .vimrc and Slack in a browser instead of installing the app for that.

On Monday, against my better judgement, I still somehow end up installing the Weechat-Slack brigde. I had read that it is kinda nice, and thought I could get away with it.

--

The next thing I know, I'm fixing this: https://github.com/wee-slack/wee-slack/issues/533
and implementing mouse handling for clickable threads, getting knee-deep into triggers: 

> thread_test: hsignal(chat_thread_open)
>              =? "${_chat_line_message} =~ Thread: (\S+) Replies"
>              ~1 ".*Thread: (\S+) Replies.*" --> "${re:1}" (_chat_line_message)
>              /1 "/command -buffer ${buffer[${tg_signal_data}].full_name} * thread ${_chat_line_message}".

Friends don't let friends do computers.

Coincidentally, the same night I started updating my computer while it was unplugged, and ended up fucking up not only grub (that boots the system) but also the kernel. Anyway, I learned how to use `chroot` to fix it, and it is objectively quite cool that such a thing is possible.

But if there is a correlation between happiness and knowing how to use `chroot`, it's a negative one.
