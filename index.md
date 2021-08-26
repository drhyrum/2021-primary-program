### Play on Youtube (may contain ads):
<a href="https://www.youtube.com/watch?v=wVBtsELKwvw&list=PLmpul3lpxxJoNbE2pRts60_ClOnIOYu7m" target="_blank"><img src="https://logodix.com/logo/360168.png" width="100"></a>

### Play in browser 

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

<li class="current-song"><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/Have%20I%20Done%20Any%20Good%20-%20Sing%20Along.mp3>Have I Done Any Good</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/I%20Know%20That%20My%20Redeemer%20Lives%20-%207-Year-Old%20Claire%20Crosby.mp3>I Know That My Redeemer Lives</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/I%20Love%20to%20See%20the%20Temple.mp3>I Love to See the Temple</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/I%20WANT%20TO%20BE%20A%20MISSIONARY%20NOW%20Lyrics%20%20Primary%20Song.mp3>I Want to be a missionary now</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/I'm%20Trying%20to%20Be%20Like%20Jesus%20Lyric%20Video.mp3>I'm Trying to Be Like Jesus</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/Jesus%20said%20Love%20everyone%20SING%20ALONG.mp3>Jesus said Love everyone</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/Joseph%20Smith%E2%80%99s%20First%20Prayer%20Hymn%20%2326%20(With%20Lyrics).mp3>Joseph Smith</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/My%20Own%20Sacred%20Grove%20(original%20song%20by%20Angie%20Killian).mp3>My Own Sacred Grove (Angie Killian)</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/Step%20by%20Step%20(a%20new%20baptism%20song%20by%20Angie%20Killian).mp3>Step by Step (Angie Killian)</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/The%20Church%20of%20Jesus%20Christ%20-%20a%20Primary%20song.mp3>The Church of Jesus Christ</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/The%20Priesthood%20Is%20Restored%20Children%E2%80%99s%20Songbook%20%2389%20(With%20Lyrics).mp3>The Priesthood Is Restored</a></li>

<li><a href=https://github.com/drhyrum/2021-primary-program/raw/main/list/When%20I%20am%20Baptized.mp3>When I am Baptized</a></li>
    
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

### QR Code to website
<img src="https://github.com/drhyrum/2021-primary-program/raw/gh-pages/primary_program_qr_code.png">


<!--
<a href="https://raw.githubusercontent.com/drhyrum/2021-primary-program/main/playlist.m3u" download="playlist.m3u">Download the playlist.</a>
-->
