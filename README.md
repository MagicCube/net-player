# netease-music
## To get playlists of a specific user
http://music.163.com/api/user/playlist/?uid=40652589&limit=1000&offset=0

## To get details of a specific playlist
http://music.163.com/api/playlist/detail?id=4000000




# qingting.fm 
## Voice of economy
http://hls.qingting.fm/live/387.m3u8?deviceid=00000000-6822-8da4-ffff-ffffca7471cb

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script src="hls.js"></script>
</head>
<body>

<audio controls id="audio"></audio>
<script>
  if(Hls.isSupported()) {
    var audio = document.getElementById('audio');
    var hls = new Hls();
    hls.loadSource('http://hls.qingting.fm/live/387.m3u8?deviceid=00000000-6822-8da4-ffff-ffffca7471cb&format=mpegts');
    hls.attachMedia(audio);
    hls.on(Hls.Events.MANIFEST_PARSED,function() {
      audio.play();
  });
 }
</script>
</body>
</html>
```
