[Back to index](../README.md)

###### I might have changed the metaRAW.html file to show my own MEI file "by mistake".

1. Create a second version of the MEI file

    A second version of my MEI file has been created as [tondikter_mei_week7.mei](../data/tondikter_mei_week7.mei).

    I had some trouble figuring out what way to add the required information in the best way possible. 

    Due to the fact that a traditional genre classification for my dataset would make everything equate to "classical" or some relatively meaningless variation of it, I am sticking with 
                
            <perfMedium>
            	<perfResList>
               	<perfRes>Piano</perfRes>
               </perfResList>
            </perfMedium>

    as the primary marker of genre, as the primary classification of different tracks happens on an insturmentation basis in my dataset.

    Licensing wise I decided to include an `<availability>` tag with a `<useRestrict>` child that specified the Public Domain ambition of the Swedish Musical Heritage archive. No specific per-work licensing exists for the archive so a generalized blanket statement was written.

2. Render the revised metadatas

    The metadata is presented in an unintelligable, raw format without any newlines or separation of any kind. The simplest way to format the data to be more readable is to clearly separate critical items by line and category of metadata heading. Names that are not in propely formatted responsibility statements are also not clearly marked as being who they are supposed to be (the composer is just a freestanding name without a label), which is something that needs fixing.

    <iframe src="../myMeta.html">
    </iframe>