---
title: Oak Hills Musical 2019-2020
---

<div class="updates" markdown="1">

# Updates
## Sunday Nov. 17th 2019
* Updated welcome
* Lion King Cast form
* Lion King Parent Handout
* Audition Info
* Youtube links to show
* Updated calendar


</div>

-----------

# Welcome!
Parents- It is time for this years Lion King Jr.! We are so excited about this show and can not wait to start it! Thank you to those who attended the parent meeting. If you have lost your parent handout and or cast form we will provide a pdf down below. A new one can also be picked up in front of the main office. We have some important dates coming up. Friday Nov. 22nd- 5th and 6th grade lead auditions. Girls- 1:30-3:00pm. Boys- 3:00-4:30pm. Boys please arrive by 2:30pm. Reminder that all dress rehearsals are mandatory. If auditioning for a lead please be sure to check your conflicts for March 6th. Performances are March 9th-13th. Lead role's will be posted outside the front office Nov. 26th. Scripts will be picked up inside the office.

# Lion King Cast Form
[Cast Form PDF](/files/Lion King Cast Form.pdf)

# Lion King Parent Handout
[Parent Handout PDF](/files/Lion King Jr. Parent Handout.pdf)

# Audition Info
Scar, Mufasa, young Simba, and old Simba will all be cast as boys. Nala, Lionesses, and Sarabi will be cast as girls. Timon, Pumbaa, Rafiki, Zazu, Shenzi, Banzai, and Ed can be cast as either boy or girl. You will find a pdf to each of the songs and lines for all the leads. We have also included an audio track of each song. If you click on the "cue for audition" it will take you to the place you start the songs. There is an option to listen to it with the vocals or without (minus track). We encourage you to learn it with the vocal and then practice it without the vocals. All auditions will be done with the minus tracks.

### Nala, Lionesses, Sarabi- Shadowland

<div class="audio-player" data-file="21 Shadowland.mp3" data-audition-start-at="80"></div>

### Rafiki- He Lives in You

<div class="audio-player" data-file="26 He Lives in You.mp3" data-audition-start-at="82.2"></div>

### Simba, Timon, Pumbaa- Hakuna Matata

<div class="audio-player" data-file="18 Hakuna Matata (Part 1).mp3" data-audition-start-at="102"></div>

### Scar and Mufasa- Be Prepared

<div class="audio-player" data-file="11 Be Prepared.mp3" data-audition-start-at="29"></div>

### Scar, Musfasa, Zazu- lines
[Scar, Mufasa, Zazu PDF](/files/auditions/Scar-Zazu-Mufasa.pdf)<br/>

### Simba and Scar- lines
[Simba and Scar PDF](/files/auditions/Simba-Scar.pdf)

### Shenzi, Banzai, Ed (Hyenas)- lines
[Hyenas PDF](/files/auditions/Hyenas.pdf)


# Youtube Show links
[Show #1](https://youtu.be/C-kFHX88Rhk)<br/>
[Show #2](https://youtu.be/3_-Uxp4sZQg)





<script>
var els = document.querySelectorAll('div.audio-player');
for (i=0; i < els.length; i++) {
  var element = els[i];
  element.dataset.index = i;

  var auditionLink = document.createElement('a');
  auditionLink.innerHTML = 'Cue for Audition';
  auditionLink.onclick = function() {
    var audioTag = Array.from(this.parentNode.getElementsByTagName('audio'));
    var visible = audioTag.filter(function(tag) {
      return tag.style.display != 'none';
    })[0];
    visible.currentTime = this.parentNode.dataset.auditionStartAt;
  }

  var audioTagA = document.createElement('audio');
  audioTagA.src = "/files/Guide Vocals/" + element.dataset.file;
  audioTagA.className = "vocals";
  audioTagA.preload = 'metadata';
  audioTagA.controls = true;

  var audioTagB = document.createElement('audio');
  audioTagB.src = "/files/Performance Tracks/" + element.dataset.file;
  audioTagB.className = "performance";
  audioTagB.preload = 'metadata';
  audioTagB.controls = true;

  audioTagA.onplay = audioTagB.onplay = function() {
    var other = this.parentNode.querySelector("audio:not(." + this.className +")");
    if (other.paused)
      other.play();
  }

  var vocalsSelection = document.createElement('select');
  vocalsSelection.innerHTML = '<option value="vocals">With Vocals</option><option value="performance">No Vocals</option>'

  vocalsSelection.onchange = function() {
    var toShow = this.parentNode.querySelector('audio.' + this.value);
    var toHide = this.parentNode.querySelector("audio:not(." + toShow.className +")");

    if (!toHide.paused)
      toShow.play();
    toShow.currentTime = toHide.currentTime;
    toShow.muted = false;
    toHide.muted = true;
    toHide.pause();

    toShow.style.display = "";
    toHide.style.display = "none";
  }


  element.appendChild(auditionLink);
  element.appendChild(vocalsSelection);
  element.appendChild(audioTagA);
  element.appendChild(audioTagB);
  vocalsSelection.onchange();
}
</script>
