---
layout: post 
title: "Video compression at the command line" 
date: 2025-05-24 
---
### I'm still here

I haven't posted anything lately, but I'm still beavering away at the
command line! I took delivery of some Raspberry Pi boards and boxes, so
I've been having some fun (and frustration!) with them. I'll write about
that another time.

My theme today is Video.

I'm no sort of video expert. I can sort of use OpenShot to get something
done, but I'm not filled with enthusiasm by the process. Until now, I've
just accepted that the output is the output, kind of take it or leave
it. But when I produced a file of 170MB that I needed to put online, I
realised I had to fill a gap in my knowledge.

That led me to discover the command `ffmpeg`.

It turns out, you can make video files smaller in the terminal. Who
knew!? It looks more complicated than doing something in a GUI editor,
but looks are deceptive - I found it to be faster and easier.

For my future reference (pretty sure no one else is reading this!),
here's the command I used and the reasoning behind it:

`ffmpeg -i input.mp4 -vcodec libx264 -crf 28 -preset veryfast -acodec aac -b:a 96k output.mp4` 

-i input.mp4: Specifies the input file  
-vcodec libx264: Tell ffmpeg to use the H.264 codec (full disclosure -
I've only the vagest sense of what that means)  
-crf 28 : crf = Constant Rate Factor, range is 0 (best quality) to 51
(worst quality, smallest file)  23-28 is recommended  
-preset veryfast : Slower presets compress better (smaller file, same quality), but take longer. Options (slowest to fastest): placebo, veryslow, slower, slow, medium (default), fast, faster, veryfast, superfast, ultrafast  
-acodec aac : s[ecifies the audio codec  
-b:a 96k : sets the audio bitrate  
output.mp4 : the output file (obvs) 
