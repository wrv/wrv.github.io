# BSidesDFW 2023
https://bsidesdfw.com/2023spkr#t31130

- [Talk (TBD)](#)
- [Slides](slides.pdf)
- [Video Generation Demo](cve_2022_32939_demo_vid_generation.mp4)
- [Playing Video on iPhone Demo](cve_2022_32939_demo_play_vid.mp4)
- [Code](https://github.com/h26forge/h26forge)

This talk covers much of the same content as the H26Forge Black Hat 2023, but includes the following changes:
- Improved explanation of manually modifying bitstreams
- Discussion around other codec-related in-the-wild exploited vulnerabilities
- More details around what RLBox is and how it can help protect media playback

## Demo Description: CVE-2022-32939
The demo is split into two parts: (1) video generation, (2) and video playback on a physical iPhone.

1. In the video generation part, I show that we take an input video that has little to no emulation prevention bytes (EPBs),
and pass it through a video transform that will expand the SPS `num_ref_frames_in_pic_order_cnt_cycle` syntax element to
insert 514 EPBs. This leads to an overwrite at 0x1fd1 bytes past the start of the EPB array, with the value 0xffff2970 
being written. 
2. In the second part, we take the generated video and transfer it to a physical 1st generation iPhone SE with iOS 13.3. During
thumbnail generation, the vulnerability will be triggered and the device will reboot. 

## Bit flipped videos
I've included the Black Hat opening sequence video as well as the actual bit flipped videos. Note that the effect we saw in the talk was because of my own video decoder, and it's possible that other devices use different error concealment strategies with different effects e.g., all gray, all black, all YUV 0x00 which looks green, or the fun rainbow effect.