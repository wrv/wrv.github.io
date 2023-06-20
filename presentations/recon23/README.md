# REcon 2023
https://cfp.recon.cx/2023/talk/9XJF7P/

- [Slides](slides.pdf)
- [Demo](demo.mp4)

## Demo Description 
The demo is a webpage that contains an overwriting context and a vulnerable context. 

The overwriting context has `autoplay` enabled so it is loaded in memory when the page opens. 
We first play the vulnerable context so it is loaded right after the overwriting context. 
Then we play the overwriting context to modify the vulnerable context. 
Finally, when we play the vulnerable context again we get a panic due to an overwritten
vtable pointer. 

## Bit flipped videos
I've included the REcon opening sequence video as well as the actual bit flipped videos. Note that the effect we saw in the talk was because of my own video decoder, and it's possible that other devices use different error concealment strategies with different effects e.g., all gray, all black, all YUV 0x00 which looks green, or the fun rainbow effect.