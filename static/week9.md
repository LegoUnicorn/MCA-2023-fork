<head>
    <title>Week 9 | MCA</title>
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
    <li><a href="../README.md">Back to index</a></li>
    <li><a href="week1.html">Week 1</a></li>
    <li><a href="week2.html">Week 2</a></li>
    <li><a href="week3.html">Week 3</a></li>
    <li><a href="week3.html">Week 4</a></li>
    <li><a href="week5.html">Week 5</a></li>
    <li><a href="week7.html">Week 7</a></li>
    <li><a href="week8.html">Week 8</a></li>
    <li><a href="week9.html">Week 9</a></li>
    <li><a href="week10.html">Week 10</a></li>
</ul>
</div>

# Task 1
1. Identify and download three music tracks relating to your portfolio theme. For each track export three feature `.csv`s and screenshots of the panes. 

    The tracks that will be used are carried over from before and can be found here:

    | ![Sonic Visualiser Galopp three panes](/static/img/galopp_week9.png) | ![Sonic Visualiser tonbilder three panes](/static/img/tonbilder_week9.png) | ![Sonic Visualiser trastens klagan three panes](/static/img/trasten_week9.png) |
    |---|---|---|
    | [Galopp.mp3](/static/audio/gallopp.mp3) |   [Tonbilder.mp3](/static/audio/tonbilder.mp3) | [Trastens Klagan.mp3](/static/audio/trastens_klagan.mp3) |
    | Adaptive spectrogram, mfcc and chromagram for Princess Eugénie Bernadotte's Tullgarn's Galopp. | Adaptive spectrogram, mfcc and chromagram for Elfrida Andrée's Fem Smärre Tonbilder. | Adaptive spectrogram, mfcc and chromagram for Laura Netzel's Trastens Klagan. |

# Task 2

1. For each track and feature type in task 1 use the `.Ipynb` to to create charts and graphs 

## Spectro



## MFCCs

| ![analysis of galopp](/static/img/galopp_analysis.png) | ![analysis of tonbilder](/static/img/tonbilder_analysis.png) | ![analysis of trastens klagan](/static/img/trasten_analysis.png) |
|---|---|---|
| Galopp | Tonbilder | Trastens Klagan |
    
## Chroma
I adapted the python code after realizing that chroma features number at 12 instead of 20. 

| ![analysis of galopp](/static/img/chro_galopp_analysis.png) | ![analysis of tonbilder](/static/img/chro_tonbilder_analysis.png) | ![analysis of trastens klagan](/static/img/chro_trasten_analysis.png) |
|---|---|---|
| Galopp | Tonbilder | Trastens Klagan |

## Comparison

All three tracks are very similar in broad strokes, all thre ehave piano as the primary instrument, they're all from the late 1800s and all self-described as some kind of chamber music. The critical difference is that track 3 also contains a female vocal. Despite this, track 2 seems to be the most radically different between the three. 