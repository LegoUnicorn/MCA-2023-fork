<head>
    <title>Week 3 | MCA</title>
</head>
<div>
    <style>
        .menu {
        list-style-type: none; 
        text-align: center;
    }
    .menu li {
        display: inline-block;
        margin-right: 10px;
    }
    </style>
    <ul class="menu">
    <li><a href="../README.html">Back to index</a></li>
    <li><a href="week1.html">Week 1</a></li>
    <li><a href="week2.html">Week 2</a></li>
    <li><a href="week3.html">Week 3</a></li>
    <li><a href="week4.html">Week 4</a></li>
    <li><a href="week5.html">Week 5</a></li>
    <li><a href="week7.html">Week 7</a></li>
    <li><a href="week8.html">Week 8</a></li>
    <li><a href="week9.html">Week 9</a></li>
    <li><a href="week10.html">Week 10</a></li>
</ul>
</div>

1. <i>Export the score you've created to MusicXML and MEI, then render using Verovio</i>

[MusicXML file](../data/tondikter_mxml.musicxml)

[MEI file](../data/tondikter_mei.mei)

2. Compare 3 elements in the MusicXML file to the corresponding MEI file. 

[Backup to Verovio.html](../verovio.html)

<iframe src="../verovio.html" width="100%" height="1000px">
</iframe>

### Copy of answers
<i>I couldn't get the verovio.html page to display anything other than the inline viewer, so i'm attaching a copy of the text I wrote to make sure it is visible:</i>

Firstly, there is a fundamental difference between the purpose of MEI and MusicXML, where MusicXML is meant to be a portable format to transfer scores between various editors, while MEI is meant to be able to represent the musical relationship between elements on a page, not just the visual. 

Understanding that there are multiple voices in the piece provides an interesting comparison between MEI and MusicXML. The first event of the music is a quaver rest in one voice and a crotchet chord in the other. The MEI groups voices in a "1" and "2" layer, with notes contained within, while the MXML file does not group them by voice, instead opting for simply grouping by measure, each measure containing all notes with voice information embedded within each note tag.

Another key difference is the prescense of positional information in the MXML file, and not in the MEI file. Whereas a chord in MXML is displayed as a series of notes being linked by their identical X-position (usually), the MEI groups notes in a chord tag that contains dduration and stem information that is shared between the notes in the chord, meaning that the note tags within the chord only contain octave and note information.

Finally, the measure tag exists in both files. However, the children of the measure tag develop very differently. To represent the F in the first chord after the rest in the third measure MEI: 

        Measure
        |Staff [1]
        ||layer [1]
        |||rest
        |||chord [duration, stem direction]
        ||||artic(ulation) [staccato]
        ||||note [octave, name] <---

In MXML, the same note would be expressed, from measure tag:

        Measure
        |note
        |note <---
        ||pitch
        |||step
        |||octave
        ||duration
        ||voice
        ||type
        ||stem
        ||Staff
        ||notations
        |||slur
        |||articualtions
        ||||staccato

In short, the same information is displayed in a "deeper" way in MEI, what allows for each step of the structure to take on some properties that affect the children. MXML on the oither hand takes a shallow approach where separate tags do the work of defining each note.

The end result is a lot more repetition in the MXML document. The MEI file is only 576 lines, while the MXML file is 2730. Even with random IDs for each tag in the MEI file, it provides a much more semantic rendition of the music than MXML does. 
