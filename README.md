### About me

I'm a software developer at, formerly under [Kinvolk](https://kinvolk.io/), now Microsoft (Azure Arc), working on [Flatcar Container Linux](https://www.flatcar-linux.org/).
I also worked on [Lokomotive](https://github.com/kinvolk/lokomotive), [Inspektor Gadget](https://github.com/kinvolk/inspektor-gadget), and [traceloop](https://github.com/kinvolk/traceloop).

As a fun interview task at Kinvolk I implemented the [idea](https://github.com/systemd/systemd/issues/10227) of a systemd option to define BPF programs as packet filters for all network sockets of a CGroup. This is now part of systemd since version 243 and lets you use a [custom network filter](https://www.freedesktop.org/software/systemd/man/systemd.resource-control.html#IPIngressFilterPath=BPF_FS_PROGRAM_PATH) for your systemd service.
Try out the examples in my [bpf-cgroup-filter](https://github.com/pothos/bpf-cgroup-filter) repo, and read the [first](https://kailueke.gitlab.io/systemd-custom-bpf-firewall/) and [second](https://kailueke.gitlab.io/systemd-bpf-firewall-loader/) blog post.

I did my dual degree Master in computer science at TU Berlin and KAIST (South Korea), where I was part of Prof. [Sue Moon's](http://an.kaist.ac.kr/~sbmoon/) [Advanced Networking Lab](http://an.kaist.ac.kr/).
I did my Bachelor in computer science at FU Berlin.
I'm part of the German association [Forum Computer Scientists for Peace and Social Responsibility](https://de.wikipedia.org/wiki/Forum_InformatikerInnen_f%C3%BCr_Frieden_und_gesellschaftliche_Verantwortung), where [Joseph Weizenbaum](https://en.wikipedia.org/wiki/Joseph_Weizenbaum) was a founding member (I recommend you to watch some of his interviews or the documentary [»Plug & Pray«](http://www.plugandpray-film.de/en/)).

My [Master's thesis](https://pothos.github.io/papers/) was about memory-safe userspace networking to protect against security vulnerabilities in the OS kernel's TCP/IP network stack due to memory corruption bugs. The solution consists of [usnetd](https://github.com/ANLAB-KAIST/usnetd) a memory-safe L4 switch to share a NIC between multiple userspace network stacks and the kernel's network stack, and [usnet_sockets](https://github.com/ANLAB-KAIST/usnet_sockets) a Rust userspace networking library based on [smoltcp](https://github.com/smoltcp-rs/smoltcp) that is still able to integrate with the loopback device. It offers various options on direct or shared NIC access. It uses my [usnet_devices](https://github.com/ANLAB-KAIST/usnet_devices) library for netmap, macvtap, and UNIX domain sockets smoltcp interfaces.

In my spare time I maintain [GNOME Disks](https://gitlab.gnome.org/GNOME/gnome-disk-utility) and implemented filesystem resize, check, and repair support for it in a [GSoC project](https://wiki.gnome.org/Outreach/SummerOfCode/2017/Projects/KaiLueke_Disks). This made me also work on [udisks](https://github.com/storaged-project/udisks) and [libblockdev](https://github.com/storaged-project/libblockdev). Please reach out if you want to improve GNOME Disks. I still have a long todo list even though I don't find the time to write new code.

I like compilers and compression, and even more if both are combined. My [Bachelor's thesis](https://pothos.github.io/papers/) was about a [compiler for a subset of Python to ZPAQL bytecode](https://github.com/pothos/zpaqlpy). [ZPAQ](http://mattmahoney.net/dc/zpaq.html) is a compression format which embeds the decompression bytecode in the archive, allowing to change the algorithm without requiring the decoder to be updated. This idea addressed the incompatibility problem that all the versions of [PAQ compressors](https://en.wikipedia.org/wiki/PAQ) had, and also allowed to choose different algorithms depending on the type of input data. However, ZPAQL wasn't used by many people because it is an assembly-like language. With a Python-like language to compile from I wanted to lower this barrier to write custom compression algorithms and also prove that the format can embed non-context modeling algorithms like Brotli (which I ported to Python from a Rust implementation). Custom algorithms are useful because the key element in data compression is prediction of future data which works best when the current context is taken into account. E.g., with ZPAQ it was easy to write a compression model for PNM image data that uses the color of the neighbor pixels to predict the next. The generated code is not the fastest because my malloc implementation isn't but it is a good playground for data compression. A fun exercise was to detect the decimal digits of Pi and then switch from a generic text compression model to perfectly predicting the next digits of Pi, essentially wasting almost no bytes on storing this seemingly random string it in a text despite it appearing like incompressible random data to any other compression algorithm.

In university I also worked on a [Twee to Z-Code](https://github.com/Drakulix/zwreec) compiler with a tracing garbage collector.
If you are into Arduinos you may find my library for [Nintendo 64 controllers](https://github.com/pothos/arduino-n64-controller-library) useful which you can try out playing a [tetris port](https://kailueke.gitlab.io/N64Tetris.zip) on your TV (or anything that displays the composite video signal the Arduino generates in software). I'll spare you my QBasic and Visual Basic code but if GitHub existed then, you would find it here ;)

I'm not actively writing on my [blog](https://kailueke.gitlab.io/) but you can find my email address there, or create an issue in this [readme repo](https://github.com/pothos/pothos) to contact me.

My GNOME Account: [gitlab.gnome.org/kailueke](https://gitlab.gnome.org/kailueke)
