# Local Media

This folder is originally created by Alexander and the media inside shall not be misused by any developer.

This local media of a short video is originally from the Alexander Ezharjan's micro-film produced in 2014.
In order to make an M3U8 live streaming from an MP4 video, Alexander's film had to be converted to `MP4` format. 
Then the [the steps for creating an M3U8 live streaming of an MP4 video](https://www.cnblogs.com/ezhar/p/13399499.html) are as follows:

1. Install [FFmpeg](https://ffmpeg.org/).

2. Type the command below to create an M3U8 file based on the converted `ts`-suffixed file pieces from MP4 video:

```bat
ffmpeg -i demo.mp4 -hls_time 10 -hls_list_size 0 -hls_segment_filename ene_%05d.ts ene.m3u8
```
3. Open your server inside this folder and visit the `*.m3u8` file to see the video of download it and view the video contents.

4. You can use LAMP or XAMPP or directly use Node.js server like the packaged command as is shown below:
```bat
npm install -g servez
servez -h
servez -p 80
```

5. Change the video addresses inside the created `M3U8` file into the server's address you created, eg. add your server's IP address ahead of the ts-suffixed videos' so that this M3U8 file downloaded from your server can be opened and viewed correctly.

<br>
<br>
<br>
<br>

by Alexander Ezharjan

