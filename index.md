---
title: Oak Hills Musical 2019-2020
---

<div class="updates" markdown="1">

# Updates
## Monday Jan. 20, 2020
* Updated welcome
* Cast and Ensemble Lists
* Updated calendar
* Lion King Cast form
* Lion King Parent Handout

</div>

-----------

## Welcome!
Parents and students. Sorry for the confusion on the music missing from the website. We are hoping to have it back by the end of the week. In the mean time you can find a link to youtube with the music to practice. We can tell the kids have been practicing and love that about them!

## Cast Lists

### Timon cast

#### Leads

Name|Part|Ensemble
-----|-----
Dane Anderson|Older Simba
Colby Anthon|Lioness|Red
Abby Bagley|Lioness|Red
Isabella Beck|Zazu
Samantha Campbell|Young Nala
Addi Cook|Shenzi
Nate Dellenbach|Young Simba
McKinley Duryea|Older Nala
Reagan Duryea|Pumbaa
Elizabeth Geilman|Lioness|Red
Samantha Godfrey|Rafiki
Thomas Hess|Ed
Samantha Jensen|Sarafina|Red
Megan Lechtenberg|Banzai
Ben Liljenquist|Mufasa
Penny Pilkington|Sarabi|Red
Lincoln Pykles|Timon
Jayda Schow|Lioness|Red
Adelaide Stevenson|Lioness|Red
Evan Torkelson|Scar

#### Ensemble

Name|Part|Ensemble
-----|-----|-----
Grant Adair|Animal|Orange
Elijah Adams|Hyena|Blue
Campbell Anderson|Animal|Green
Sage Anderson|Animal|Green
Ben Bagley|Animal|Orange
Greyson Birchard|Animal|Green
Lindsey Bleazard|Animal|Green
Luke Bleazard|Animal|Green
Ryan Bleazard|Stage crew|
Bridger Bronson|Hyena|Blue
Trinton Christensen|Hyena|Blue
Davis Duke|Animal|Orange
Emma Dellenbach|Animal|Green
Amelia Geilman|Hyena|Blue
Kylie Goodell|Stage crew|
Matthew Hess|Animal|Green
Carter Halladay|Animal|Orange
Mabel Hutchings|Animal|Orange
Peter Hutchings|Animal|Orange
Audrey Jensen|Animal|Orange
Ella Jensen|Animal|Green
Elin Johanson|Animal|Green
Amelia Johnson|Animal|Orange
Kove Larsen|Animal|Green
Kylie Larsen|Hyena|Blue
Eden Liljenquist|Hyena|Blue
Amelia Lyman|Animal|Orange
Ammon Madsen|Animal|Orange
Jane Meidell|Hyena|Blue
Liesel Mickelson|Animal|Orange
Nels Mickelson|Animal|Orange
Lucas Morrow|Animal|Green
Mathias Morrow|Animal|Orange
Sophia Morrow|Hyena|Blue
Blakely Nelsin|Animal|Orange
Ivy Pace|Animal|Green
Lucy Pace|Animal|Green
Casey Randall|Hyena|Blue
Kaitlin Robert|Hyena|Blue
Izzy Smoot|Animal|Orange
Mason Stewart|Animal|Green
Aaron Tibbitts|Animal|green
Brandon Tibbitts|Animal|Green
Millicent Trevino|Stage Crew
Matthew Young|Animal|Orange
Sadie Young|Animal|Orange

### Pumbaa cast

#### Leads

Name|Part|Ensemble
-----|-----
Kymber Best|Lioness|Red
Henry Brown|Young Simba
McKenna Cone|Shenzi
Mathilda Cottam|Rafiki
Samuel Frei|Banzai
Kirsti Holzer|Lioness|Red
Jorja Hone|Lioness|Red
Sabrina Layne|Sarafina|Red
Porter Murdock|Timon
Lily Olson|Lioness|Red
Mac Pickett|Pumbaa
Bea Richards|Sarabi|Red
Jack Rose|Scar
Saphirah Simmons|Older Nala
Caleb Taylor|Ed
Carter Terry|Older Simba
Afton Vail|Lioness|Red
Daxton Wilson|Mufasa
Luke Wright|Zazu
Alayna Yoho|Young Nala

#### Ensemble

Name|Part|Ensemble
-----|-----|-----
William Barker|Hyena|Blue
Sailor Beyer|Hyena|Blue
Luke Bleazard|Animal|Green
Simon Brady|Animal|Green
Lily Bremner|Hyena|Blue
Chloe Bryson|Stage crew|
Kylee Corbett|Hyena|Blue
Henry Cottam|Animal|Green
Claire Dodds|Stage Crew
Kate Dodds|Hyena|Blue
Brooklyn Dodge|Hyena|Blue
Heidi Ence|Animal|Orange
Max Ence|Hyena|Blue
Lena Frei|Animal|Green
Logan Fuller|Hyena|Blue
Beck Green|Animal|Orange
Brinley Green|Hyena|Blue
Corbin Heath|Animal|Green
Markus Holzer|Animal|Orange
Ava Howe|Animal|Green
Layla Jewkes|Animal|Orange
Kaydence Kupfer|Animal|Green
Damie LeFever|Animal|Orange
Sabrina Lunceford|Animal|Orange
Molly Lynn|Animal|Orange
Mina Marriot|Animal|Green
Zuri Monson|Animal|Orange
Amelia Olson|Animal|Green
Sam Richards|Animal|Orange
Scarlet Rupp|Animail|Green
Max Rose|Animal|Orange
Aspen Smith|Animal|Orange
Reed Stevens|Stage crew|
Leah Taylor|Animal|Orange
Audri Terry|Animal|Green
Ara Terry|Hyena|Blue
Beck Terry|Animal|Orange
Drew Terry|Animal|Orange
Jeffery Thiriot|Animal|Green
Leilani Walker|Animal|Orange
Emily Wellard|Animal|Green
Seth Wright|Animal|Green
Chuck Yates|Animal|Green

## Youtube Music Link
[Lion King Music](https://www.youtube.com/watch?v=ET8WA9rlEIU&list=PLLb1A1sS2On9zLgW9Drfbo4s6jMSHQqiY)

## Youtube Show Links
[Show #1](https://youtu.be/C-kFHX88Rhk)<br/>
[Show #2](https://youtu.be/3_-Uxp4sZQg)

## Lion King Cast Form
[Cast Form PDF](/files/Lion King Cast Form.pdf)

## Lion King Parent Handout
[Parent Handout PDF](/files/Lion King Jr. Parent Handout.pdf)

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


  if (element.dataset.auditionStartAt) {
    element.appendChild(auditionLink);
  }
  element.appendChild(vocalsSelection);
  element.appendChild(audioTagA);
  element.appendChild(audioTagB);
  vocalsSelection.onchange();
}
</script>
