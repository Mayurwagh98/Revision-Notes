1. Create a new HTML file or open an existing one in your text editor.
2. Inside the body element, add the video or audio element depending on whether you want to play a video or audio file. The basic syntax for both tags is similar:
```
<video controls>
  <source src="path/to/video.mp4" type="video/mp4">
  <source src="path/to/video.webm" type="video/webm">
  Your browser does not support the video tag.
</video>
```
```
<audio controls>
  <source src="path/to/audio.mp3" type="audio/mpeg">
  <source src="path/to/audio.ogg" type="audio/ogg">
  Your browser does not support the audio tag.
</audio>
```
3. In the above examples, the controls attribute adds playback controls to the video or audio player. The source element specifies the file path and file type of the video or audio file to be played. The last line inside the tag is fallback content that will be displayed if the browser does not support the video or audio element.
4. Save the file and open it in your web browser. You should see the video or audio player with playback controls and the file should start playing when you click the play button.
