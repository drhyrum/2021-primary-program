## 2021 Primary Program
<a href="https://raw.githubusercontent.com/drhyrum/2021-primary-program/main/playlist.m3u" download>Download the playlist.</a>

# 2021-primary-program
<style>
    #playlist{
        list-style: none;
    }
    #playlist li a{
        color:black;
        text-decoration: none;
    }
    #playlist .current-song a{
        color:blue;
    }
</style>

<audio src="" controls id="audioPlayer">
    Sorry, your browser doesn't support html!
</audio>
<ul id="playlist">

<li class="current-song"><a href="https://github.com/drhyrum/2021-primary-program/raw/main/list/Step%20by%20Step%20(a%20new%20baptism%20song%20by%20Angie%20Killian).mp3
">Step by Step</a></li>

<li><a href="https://github.com/drhyrum/2021-primary-program/raw/main/list/Joseph%20Smith%E2%80%99s%20First%20Prayer%20Hymn%20%2326%20(With%20Lyrics).mp3
https://github.com/drhyrum/2021-primary-program/raw/main/list/Joseph%20Smith%E2%80%99s%20First%20Prayer%20Hymn%20%2326%20(With%20Lyrics).mp3">Joseph Smith's First Prayer</a></li>

<li><a href="https://github.com/drhyrum/2021-primary-program/raw/main/list/My%20Own%20Sacred%20Grove%20(original%20song%20by%20Angie%20Killian)%20(1).mp3
">My Own Sacred Grove</a></li>

</ul>

<script src="https://code.jquery.com/jquery-2.2.0.js">
</script>
<script>
    // loads the audio player
    audioPlayer();

       function audioPlayer(){
            var currentSong = 0;
            $("#audioPlayer")[0].src = $("#playlist li a")[0];
            $("#audioPlayer")[0].play();
            $("#playlist li a").click(function(e){
               e.preventDefault(); 
               $("#audioPlayer")[0].src = this;
               $("#audioPlayer")[0].play();
               $("#playlist li").removeClass("current-song");
                currentSong = $(this).parent().index();
                $(this).parent().addClass("current-song");
            });
            
            $("#audioPlayer")[0].addEventListener("ended", function(){
               currentSong++;
                if(currentSong == $("#playlist li a").length)
                    currentSong = 0;
                $("#playlist li").removeClass("current-song");
                $("#playlist li:eq("+currentSong+")").addClass("current-song");
                $("#audioPlayer")[0].src = $("#playlist li a")[currentSong].href;
                $("#audioPlayer")[0].play();
            });
        }    
</script>


All files were sourced from https://youtube.com/


