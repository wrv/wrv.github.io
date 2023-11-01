# Demuxed 2023
https://2023.demuxed.com/

**Having H26Fun with H26Forge: Vulnerability Hunting, Datamoshing, and More!**

Description
> Modern video encoding standards such as H.264 are a marvel of hidden complexity. But with hidden complexity comes hidden security risk. Decoding video today involves interacting with dedicated hardware accelerators and the proprietary, privileged software components used to drive them. The video decoder ecosystem is obscure, opaque, diverse, highly privileged, largely untested, and highly exposed -- a dangerous combination.
> We introduce H26Forge, a framework that carefully crafts video files to expose edge cases in H.264 decoders. H26Forge's key insight is operating on the syntax elements rather than on the encoded bitstring to build syntactically correct but semantically spec-non-compliant video files. These files cause H.264 decoders to find themselves in undefined states or unhandled errors.
> We used H26Forge to uncover numerous vulnerabilities across the video decoder ecosystem, including kernel memory corruption bugs in iOS, memory corruption bugs in Firefox and VLC for Windows, and video accelerator and application processor kernel memory bugs in multiple Android devices. These bugs have been acknowledged by multiple vendors including Apple, Mozilla, and FFmpeg.
> In this talk, we will describe how H26Forge can be used to find issues that may arise in processing User Generated Content so that video engineers can protect their infrastructure. We will also discuss other uses of H26Forge, such as debugging encoded videos or datamoshing.


- [Talk (TBD)](#)
- [Slides(PDF)](slides.pdf)
- [Slides(Google Slides)](https://docs.google.com/presentation/d/1kpdRdhFwtaolvYIuHSWb6aIf8l-j3leU0W_S4njmAtM/edit?usp=sharing)
- [Code](https://github.com/h26forge/h26forge)
- [Datamoshing transforms](https://github.com/h26forge/h26forge/tree/main/transforms/datamoshing)