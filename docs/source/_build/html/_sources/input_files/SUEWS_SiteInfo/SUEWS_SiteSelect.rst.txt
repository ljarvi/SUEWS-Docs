SUEWS_SiteSelect.txt
~~~~~~~~~~~~~~~~~~~~

For each year and each grid, site specific surface cover information and
other input parameters is provided to SUEWS by **SUEWS_SiteSelect.txt**.
The model currently requires a new row for each year of the model run.
All rows in this file (before the two rows of '-9') will be read by the
model and run. In this file the **column order is important**. '!' can
be used to indicate comments in the file. Comments are not read by the
programme so they can be used by the user to provide notes for their
interpretation of the contents. This is strongly recommended.

+-----+-------+---------+---------+-----------+---------+-----+
| No. | Use   | Column  | Example | Descrip   |         |     |
|     |       | name    |         | tion      |         |     |
+=====+=======+=========+=========+===========+=========+=====+
| 1   | MU    | Grid    | 1       | Grid      | ''')    |     |
|     |       |         |         | number    | The two |     |
|     |       |         |         | (any      | last    |     |
|     |       |         |         | integer   | lines   |     |
|     |       |         |         | 0-2,147   | in this |     |
|     |       |         |         | ,483,64   | column  |     |
|     |       |         |         | 7         | must    |     |
|     |       |         |         | (larges   | read    |     |
|     |       |         |         | t         | '-9' to |     |
|     |       |         |         | 4-byte    | indicat |     |
|     |       |         |         | integer   | e       |     |
|     |       |         |         | ))        | that    |     |
|     |       |         |         | identif   | the     |     |
|     |       |         |         | ying      | last    |     |
|     |       |         |         | the       | lines   |     |
|     |       |         |         | current   | have    |     |
|     |       |         |         | grid.     | been    |     |
|     |       |         |         | -  Grid   | reached |     |
|     |       |         |         | numb      | (using  |     |
|     |       |         |         | ers       | two     |     |
|     |       |         |         | do        | lines   |     |
|     |       |         |         | not       | allows  |     |
|     |       |         |         | need      | differe |     |
|     |       |         |         | to        | nces    |     |
|     |       |         |         | be        | in      |     |
|     |       |         |         | cons      | compute |     |
|     |       |         |         | ecutive   | r       |     |
|     |       |         |         | and       | file    |     |
|     |       |         |         | do        | savings |     |
|     |       |         |         | not       | to be   |     |
|     |       |         |         | need      | dealt   |     |
|     |       |         |         | to        | with).  |     |
|     |       |         |         | star      |         |     |
|     |       |         |         | t         |         |     |
|     |       |         |         | at a      |         |     |
|     |       |         |         | part      |         |     |
|     |       |         |         | icular    |         |     |
|     |       |         |         | valu      |         |     |
|     |       |         |         | e.        |         |     |
|     |       |         |         | -  Each   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | have      |         |     |
|     |       |         |         | a         |         |     |
|     |       |         |         | uniq      |         |     |
|     |       |         |         | ue        |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | numb      |         |     |
|     |       |         |         | er.       |         |     |
|     |       |         |         | -  All    |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | pres      |         |     |
|     |       |         |         | ent       |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | all       |         |     |
|     |       |         |         | year      |         |     |
|     |       |         |         | s.        |         |     |
|     |       |         |         | \*These   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | numbers   |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | referre   |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | to in     |         |     |
|     |       |         |         | GridCon   |         |     |
|     |       |         |         | nection   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | (column   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | 64-79)    |         |     |
|     |       |         |         | ('''N.B   |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | GridCon   |         |     |
|     |       |         |         | nection   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | not       |         |     |
|     |       |         |         | current   |         |     |
|     |       |         |         | ly        |         |     |
|     |       |         |         | impleme   |         |     |
|     |       |         |         | nted      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 2   | MU    | Year    | 2011    | Year      |         |     |
|     |       |         |         | [YYYY]    |         |     |
|     |       |         |         | Years     |         |     |
|     |       |         |         | must be   |         |     |
|     |       |         |         | continu   |         |     |
|     |       |         |         | ous.      |         |     |
|     |       |         |         | If        |         |     |
|     |       |         |         | running   |         |     |
|     |       |         |         | multipl   |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | years,    |         |     |
|     |       |         |         | ensure    |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | rows in   |         |     |
|     |       |         |         | SiteSel   |         |     |
|     |       |         |         | ect.txt   |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | arrange   |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | so that   |         |     |
|     |       |         |         | all       |         |     |
|     |       |         |         | grids     |         |     |
|     |       |         |         | for a     |         |     |
|     |       |         |         | particu   |         |     |
|     |       |         |         | lar       |         |     |
|     |       |         |         | year      |         |     |
|     |       |         |         | appear    |         |     |
|     |       |         |         | on        |         |     |
|     |       |         |         | consecu   |         |     |
|     |       |         |         | tive      |         |     |
|     |       |         |         | lines     |         |     |
|     |       |         |         | (rather   |         |     |
|     |       |         |         | than      |         |     |
|     |       |         |         | groupin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | all       |         |     |
|     |       |         |         | years     |         |     |
|     |       |         |         | togethe   |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | for a     |         |     |
|     |       |         |         | particu   |         |     |
|     |       |         |         | lar       |         |     |
|     |       |         |         | grid).    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 3   | MU    | StartDL | 86      | Start     | Day     |     |
|     |       | S       |         | of the    | Light   |     |
|     |       |         |         | day       | Savings |     |
|     |       |         |         | light     | ]].     |     |
|     |       |         |         | savings   |         |     |
|     |       |         |         | [DOY]     |         |     |
|     |       |         |         | See       |         |     |
|     |       |         |         | section   |         |     |
|     |       |         |         | on        |         |     |
|     |       |         |         | [[#Day    |         |     |
|     |       |         |         | Light     |         |     |
|     |       |         |         | Savings   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 4   | MU    | EndDLS  | 303     | End of    | Day     |     |
|     |       |         |         | the day   | Light   |     |
|     |       |         |         | light     | Savings |     |
|     |       |         |         | savings   | ]].     |     |
|     |       |         |         | [DOY]     |         |     |
|     |       |         |         | See       |         |     |
|     |       |         |         | section   |         |     |
|     |       |         |         | on        |         |     |
|     |       |         |         | [[#Day    |         |     |
|     |       |         |         | Light     |         |     |
|     |       |         |         | Savings   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 5   | MU    | lat     | 60.00   | Latitud   |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | for the   |         |     |
|     |       |         |         | centre    |         |     |
|     |       |         |         | of the    |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | [decima   |         |     |
|     |       |         |         | l         |         |     |
|     |       |         |         | degrees   |         |     |
|     |       |         |         | ]         |         |     |
|     |       |         |         | -  Use    |         |     |
|     |       |         |         | coor      |         |     |
|     |       |         |         | dinate    |         |     |
|     |       |         |         | syst      |         |     |
|     |       |         |         | em        |         |     |
|     |       |         |         | WGS8      |         |     |
|     |       |         |         | 4.        |         |     |
|     |       |         |         | -  Posi   |         |     |
|     |       |         |         | tive      |         |     |
|     |       |         |         | valu      |         |     |
|     |       |         |         | es        |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | nort      |         |     |
|     |       |         |         | hern      |         |     |
|     |       |         |         | hemi      |         |     |
|     |       |         |         | sphere    |         |     |
|     |       |         |         | (neg      |         |     |
|     |       |         |         | ative     |         |     |
|     |       |         |         | sout      |         |     |
|     |       |         |         | hern      |         |     |
|     |       |         |         | hemi      |         |     |
|     |       |         |         | sphere)   |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | -  Used   |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | radi      |         |     |
|     |       |         |         | ation     |         |     |
|     |       |         |         | calc      |         |     |
|     |       |         |         | ulation   |         |     |
|     |       |         |         | s.        |         |     |
|     |       |         |         | -  Note   |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | if        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | tota      |         |     |
|     |       |         |         | l         |         |     |
|     |       |         |         | mode      |         |     |
|     |       |         |         | lled      |         |     |
|     |       |         |         | area      |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | smal      |         |     |
|     |       |         |         | l         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | lati      |         |     |
|     |       |         |         | tude      |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | long      |         |     |
|     |       |         |         | itude     |         |     |
|     |       |         |         | coul      |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | same      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | each      |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | smal      |         |     |
|     |       |         |         | l         |         |     |
|     |       |         |         | diff      |         |     |
|     |       |         |         | erences   |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | radi      |         |     |
|     |       |         |         | ation     |         |     |
|     |       |         |         | will      |         |     |
|     |       |         |         | not       |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | dete      |         |     |
|     |       |         |         | rmined.   |         |     |
|     |       |         |         | If        |         |     |
|     |       |         |         | you       |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | defi      |         |     |
|     |       |         |         | ning      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | lati      |         |     |
|     |       |         |         | tude      |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | long      |         |     |
|     |       |         |         | itude     |         |     |
|     |       |         |         | diff      |         |     |
|     |       |         |         | erently   |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | make      |         |     |
|     |       |         |         | cert      |         |     |
|     |       |         |         | ain       |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | you       |         |     |
|     |       |         |         | prov      |         |     |
|     |       |         |         | ide       |         |     |
|     |       |         |         | enou      |         |     |
|     |       |         |         | gh        |         |     |
|     |       |         |         | deci      |         |     |
|     |       |         |         | mal       |         |     |
|     |       |         |         | plac      |         |     |
|     |       |         |         | es.       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 6   | MU    | lng     | -18.20  | Longitu   |         |     |
|     |       |         |         | de        |         |     |
|     |       |         |         | for the   |         |     |
|     |       |         |         | centre    |         |     |
|     |       |         |         | of the    |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | [decima   |         |     |
|     |       |         |         | l         |         |     |
|     |       |         |         | degrees   |         |     |
|     |       |         |         | ]         |         |     |
|     |       |         |         | -  Use    |         |     |
|     |       |         |         | coor      |         |     |
|     |       |         |         | dinate    |         |     |
|     |       |         |         | syst      |         |     |
|     |       |         |         | em        |         |     |
|     |       |         |         | WGS8      |         |     |
|     |       |         |         | 4.        |         |     |
|     |       |         |         | -  For    |         |     |
|     |       |         |         | comp      |         |     |
|     |       |         |         | atibili   |         |     |
|     |       |         |         | ty        |         |     |
|     |       |         |         | with      |         |     |
|     |       |         |         | GIS,      |         |     |
|     |       |         |         | nega      |         |     |
|     |       |         |         | tive      |         |     |
|     |       |         |         | valu      |         |     |
|     |       |         |         | es        |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | west      |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | posi      |         |     |
|     |       |         |         | tive      |         |     |
|     |       |         |         | valu      |         |     |
|     |       |         |         | es        |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | east      |         |     |
|     |       |         |         | (e.g      |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | Vanc      |         |     |
|     |       |         |         | ouver     |         |     |
|     |       |         |         | =         |         |     |
|     |       |         |         | -123      |         |     |
|     |       |         |         | .12;      |         |     |
|     |       |         |         | Shan      |         |     |
|     |       |         |         | ghai      |         |     |
|     |       |         |         | =         |         |     |
|     |       |         |         | 121.      |         |     |
|     |       |         |         | 47)       |         |     |
|     |       |         |         | **No      |         |     |
|     |       |         |         | te        |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | is a      |         |     |
|     |       |         |         | chan      |         |     |
|     |       |         |         | ge        |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | sign      |         |     |
|     |       |         |         | conv      |         |     |
|     |       |         |         | ention    |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | v201      |         |     |
|     |       |         |         | 6a        |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | v201      |         |     |
|     |       |         |         | 7a**      |         |     |
|     |       |         |         | -  See    |         |     |
|     |       |         |         | lati      |         |     |
|     |       |         |         | tude      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | more      |         |     |
|     |       |         |         | deta      |         |     |
|     |       |         |         | ils.      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 7   | MU    | Timezon | 0       | Time      |         |     |
|     |       | e       |         | zone      |         |     |
|     |       |         |         | [h] for   |         |     |
|     |       |         |         | site      |         |     |
|     |       |         |         | relativ   |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | to UTC    |         |     |
|     |       |         |         | (east     |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | positiv   |         |     |
|     |       |         |         | e).       |         |     |
|     |       |         |         | This      |         |     |
|     |       |         |         | should    |         |     |
|     |       |         |         | be set    |         |     |
|     |       |         |         | accordi   |         |     |
|     |       |         |         | ng        |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | times     |         |     |
|     |       |         |         | given     |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | meteoro   |         |     |
|     |       |         |         | logical   |         |     |
|     |       |         |         | forcing   |         |     |
|     |       |         |         | file(s)   |         |     |
|     |       |         |         | .         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 8   | MU    | Surface | 75.3    | Area of   |         |     |
|     |       | Area    |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | [ha].     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 9   | MU    | Alt     | 25.0    | Altitud   |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | [m]       |         |     |
|     |       |         |         | Mean      |         |     |
|     |       |         |         | topogra   |         |     |
|     |       |         |         | phic      |         |     |
|     |       |         |         | height    |         |     |
|     |       |         |         | above     |         |     |
|     |       |         |         | sea-lev   |         |     |
|     |       |         |         | el.       |         |     |
|     |       |         |         | -  Used   |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | both      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | radi      |         |     |
|     |       |         |         | ation     |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s.        |         |     |
|     |       |         |         | (**N      |         |     |
|     |       |         |         | .B.       |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | not       |         |     |
|     |       |         |         | curr      |         |     |
|     |       |         |         | ently     |         |     |
|     |       |         |         | impl      |         |     |
|     |       |         |         | emented   |         |     |
|     |       |         |         | .**)      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 10  | MU    | z       | 20.5    | Height    |         |     |
|     |       |         |         | [m] of    |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | meteoro   |         |     |
|     |       |         |         | logical   |         |     |
|     |       |         |         | forcing   |         |     |
|     |       |         |         | data.     |         |     |
|     |       |         |         | The       |         |     |
|     |       |         |         | most      |         |     |
|     |       |         |         | importa   |         |     |
|     |       |         |         | nt        |         |     |
|     |       |         |         | height    |         |     |
|     |       |         |         | is that   |         |     |
|     |       |         |         | of the    |         |     |
|     |       |         |         | wind      |         |     |
|     |       |         |         | speed     |         |     |
|     |       |         |         | measure   |         |     |
|     |       |         |         | ment.     |         |     |
|     |       |         |         | -  z      |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | grea      |         |     |
|     |       |         |         | ter       |         |     |
|     |       |         |         | than      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | disp      |         |     |
|     |       |         |         | lacemen   |         |     |
|     |       |         |         | t         |         |     |
|     |       |         |         | heig      |         |     |
|     |       |         |         | ht.       |         |     |
|     |       |         |         | -  Forc   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | data      |         |     |
|     |       |         |         | shou      |         |     |
|     |       |         |         | ld        |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | repr      |         |     |
|     |       |         |         | esentat   |         |     |
|     |       |         |         | ive       |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | loca      |         |     |
|     |       |         |         | l-scale   |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | i.e.      |         |     |
|     |       |         |         | abov      |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | heig      |         |     |
|     |       |         |         | ht        |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | roug      |         |     |
|     |       |         |         | hness     |         |     |
|     |       |         |         | elem      |         |     |
|     |       |         |         | ents.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 11  | MD    | id      | 1       | Day       |         |     |
|     |       |         |         | [DOY]     |         |     |
|     |       |         |         | Not       |         |     |
|     |       |         |         | used:     |         |     |
|     |       |         |         | set to    |         |     |
|     |       |         |         | 1 in      |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | version   |         |     |
|     |       |         |         | .         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 12  | MD    | ih      | 0       | Hour      |         |     |
|     |       |         |         | [H] Not   |         |     |
|     |       |         |         | used:     |         |     |
|     |       |         |         | set to    |         |     |
|     |       |         |         | 0 in      |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | version   |         |     |
|     |       |         |         | .         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 13  | MD    | imin    | 0       | Minute    |         |     |
|     |       |         |         | [M] Not   |         |     |
|     |       |         |         | used:     |         |     |
|     |       |         |         | set to    |         |     |
|     |       |         |         | 0 in      |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | version   |         |     |
|     |       |         |         | .         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 14  | MU    | Fr_Pave | 0.20    | Surface   |         |     |
|     |       | d       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | Areal     |         |     |
|     |       |         |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | (roads,   |         |     |
|     |       |         |         | pavemen   |         |     |
|     |       |         |         | ts,       |         |     |
|     |       |         |         | car       |         |     |
|     |       |         |         | parks).   |         |     |
|     |       |         |         | e.g.      |         |     |
|     |       |         |         | 20% of    |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid is   |         |     |
|     |       |         |         | covered   |         |     |
|     |       |         |         | with      |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s.        |         |     |
|     |       |         |         | -  **Co   |         |     |
|     |       |         |         | lumns     |         |     |
|     |       |         |         | 14        |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | 20        |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | sum       |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | 1**.      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 15  | MU    | Fr_Bldg | 0.20    | Surface   |         |     |
|     |       | s       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | gs        |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 16  | MU    | Fr_EveT | 0.10    | Surface   |         |     |
|     |       | r       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | evergre   |         |     |
|     |       |         |         | en        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | shrubs    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 17  | MU    | Fr_DecT | 0.10    | Surface   |         |     |
|     |       | r       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | deciduo   |         |     |
|     |       |         |         | us        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | shrubs    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 18  | MU    | Fr_Gras | 0.30    | Surface   |         |     |
|     |       | s       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | grass     |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 19  | MU    | Fr_Bsoi | 0.05    | Surface   |         |     |
|     |       | l       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of bare   |         |     |
|     |       |         |         | soil or   |         |     |
|     |       |         |         | unmanag   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | land      |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 20  | MU    | Fr_Wate | 0.05    | Surface   |         |     |
|     |       | r       |         | cover     |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of open   |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | (e.g.     |         |     |
|     |       |         |         | river,    |         |     |
|     |       |         |         | lakes,    |         |     |
|     |       |         |         | ponds,    |         |     |
|     |       |         |         | swimmin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | pools)    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 21  | MU    | IrrFr_E | 0.50    | Fractio   |         |     |
|     |       | veTr    |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | evergre   |         |     |
|     |       |         |         | en        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | e.g.      |         |     |
|     |       |         |         | 50% of    |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | evergre   |         |     |
|     |       |         |         | en        |         |     |
|     |       |         |         | trees/s   |         |     |
|     |       |         |         | hrubs     |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ed        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 22  | MU    | IrrFr_D | 0.20    | Fractio   |         |     |
|     |       | ecTr    |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | deciduo   |         |     |
|     |       |         |         | us        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | are       |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 23  | MU    | IrrFr_G | 0.70    | Fractio   |         |     |
|     |       | rass    |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | grass     |         |     |
|     |       |         |         | that is   |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 24  | MU    | H_Bldgs | 10      | Mean      |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | height    |         |     |
|     |       |         |         | [m]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 25  | MU    | H_EveTr | 15      | Mean      |         |     |
|     |       |         |         | height    |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | evergre   |         |     |
|     |       |         |         | en        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | [m]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 26  | MU    | H_DecTr | 15      | Mean      |         |     |
|     |       |         |         | height    |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | deciduo   |         |     |
|     |       |         |         | us        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | [m]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 27  | O     | z0      | 0.6     | Roughne   | RunCont |     |
|     |       |         |         | ss        | rol.nml |     |
|     |       |         |         | length    | ]];     |     |
|     |       |         |         | for       | otherwi |     |
|     |       |         |         | momentu   | se      |     |
|     |       |         |         | m         | set to  |     |
|     |       |         |         | [m]       | '-999'  |     |
|     |       |         |         | Value     | and a   |     |
|     |       |         |         | supplie   | value   |     |
|     |       |         |         | d         | will be |     |
|     |       |         |         | here is   | calcula |     |
|     |       |         |         | used if   | ted     |     |
|     |       |         |         | RoughLe   | by the  |     |
|     |       |         |         | nMomMet   | model   |     |
|     |       |         |         | hod       | (RoughL |     |
|     |       |         |         | = 1 in    | enMomMe |     |
|     |       |         |         | [[#RunC   | thod    |     |
|     |       |         |         | ontrol.   | = 2,    |     |
|     |       |         |         | nml       | 3).     |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 28  | O     | zd      | 1.5     | Zero-pl   | RunCont |     |
|     |       |         |         | ane       | rol.nml |     |
|     |       |         |         | displac   | ]];     |     |
|     |       |         |         | ement     | otherwi |     |
|     |       |         |         | [m]       | se      |     |
|     |       |         |         | Value     | set to  |     |
|     |       |         |         | supplie   | '-999'  |     |
|     |       |         |         | d         | and a   |     |
|     |       |         |         | here is   | value   |     |
|     |       |         |         | used if   | will be |     |
|     |       |         |         | RoughLe   | calcula |     |
|     |       |         |         | nMomMet   | ted     |     |
|     |       |         |         | hod       | by the  |     |
|     |       |         |         | = 1 in    | model   |     |
|     |       |         |         | [[#RunC   | (RoughL |     |
|     |       |         |         | ontrol.   | enMomMe |     |
|     |       |         |         | nml       | thod    |     |
|     |       |         |         |           | = 2,    |     |
|     |       |         |         |           | 3).     |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 29  | O     | FAI_Bld | 0.1     | Frontal   | RunCont |     |
|     |       | gs      |         | area      | rol.nml |     |
|     |       |         |         | index     | ]].     |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | gs        |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | Require   |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | if        |         |     |
|     |       |         |         | RoughLe   |         |     |
|     |       |         |         | nMomMet   |         |     |
|     |       |         |         | hod       |         |     |
|     |       |         |         | = 3 in    |         |     |
|     |       |         |         | [[#RunC   |         |     |
|     |       |         |         | ontrol.   |         |     |
|     |       |         |         | nml       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 30  | O     | FAI_Eve | 0.2     | Frontal   | RunCont |     |
|     |       | Tr      |         | area      | rol.nml |     |
|     |       |         |         | index     | ]].     |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | evergre   |         |     |
|     |       |         |         | en        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | Require   |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | if        |         |     |
|     |       |         |         | RoughLe   |         |     |
|     |       |         |         | nMomMet   |         |     |
|     |       |         |         | hod       |         |     |
|     |       |         |         | = 3 in    |         |     |
|     |       |         |         | [[#RunC   |         |     |
|     |       |         |         | ontrol.   |         |     |
|     |       |         |         | nml       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 31  | O     | FAI_Dec | 0.2     | Frontal   | RunCont |     |
|     |       | Tr      |         | area      | rol.nml |     |
|     |       |         |         | index     | ]].     |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | deciduo   |         |     |
|     |       |         |         | us        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | Require   |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | if        |         |     |
|     |       |         |         | RoughLe   |         |     |
|     |       |         |         | nMomMet   |         |     |
|     |       |         |         | hod       |         |     |
|     |       |         |         | = 3 in    |         |     |
|     |       |         |         | [[#RunC   |         |     |
|     |       |         |         | ontrol.   |         |     |
|     |       |         |         | nml       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 32  | O     | PopDens | 30.7    | Daytime   | RunCont |     |
|     |       | Day     |         | populat   | rol.nml |     |
|     |       |         |         | ion       | ]].     |     |
|     |       |         |         | density   | The     |     |
|     |       |         |         | (i.e.     | model   |     |
|     |       |         |         | workers   | will    |     |
|     |       |         |         | ,         | use the |     |
|     |       |         |         | tourist   | average |     |
|     |       |         |         | s)        | of      |     |
|     |       |         |         | [people   | daytime |     |
|     |       |         |         | ha\ :su   | and     |     |
|     |       |         |         | p:`-1`]   | night-t |     |
|     |       |         |         | Populat   | ime     |     |
|     |       |         |         | ion       | populat |     |
|     |       |         |         | density   | ion     |     |
|     |       |         |         | is        | densiti |     |
|     |       |         |         | require   | es,     |     |
|     |       |         |         | d         | unless  |     |
|     |       |         |         | if        | only    |     |
|     |       |         |         | Anthrop   | one is  |     |
|     |       |         |         | HeatMet   | provide |     |
|     |       |         |         | hod       | d.      |     |
|     |       |         |         | = 2 in    | If      |     |
|     |       |         |         | [[#RunC   | daytime |     |
|     |       |         |         | ontrol.   | populat |     |
|     |       |         |         | nml       | ion     |     |
|     |       |         |         |           | density |     |
|     |       |         |         |           | is      |     |
|     |       |         |         |           | unknown |     |
|     |       |         |         |           | ,       |     |
|     |       |         |         |           | set to  |     |
|     |       |         |         |           | -999.   |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 33  | O     | PopDens | 10.2    | Night-t   | RunCont |     |
|     |       | Night   |         | ime       | rol.nml |     |
|     |       |         |         | populat   | ]].     |     |
|     |       |         |         | ion       | The     |     |
|     |       |         |         | density   | model   |     |
|     |       |         |         | (i.e.     | will    |     |
|     |       |         |         | residen   | use the |     |
|     |       |         |         | ts)       | average |     |
|     |       |         |         | [people   | of      |     |
|     |       |         |         | ha\ :su   | daytime |     |
|     |       |         |         | p:`-1`]   | and     |     |
|     |       |         |         | Populat   | night-t |     |
|     |       |         |         | ion       | ime     |     |
|     |       |         |         | density   | populat |     |
|     |       |         |         | is        | ion     |     |
|     |       |         |         | require   | densiti |     |
|     |       |         |         | d         | es,     |     |
|     |       |         |         | if        | unless  |     |
|     |       |         |         | Anthrop   | only    |     |
|     |       |         |         | HeatMet   | one is  |     |
|     |       |         |         | hod       | provide |     |
|     |       |         |         | = 2 in    | d.      |     |
|     |       |         |         | [[#RunC   | If      |     |
|     |       |         |         | ontrol.   | night-t |     |
|     |       |         |         | nml       | ime     |     |
|     |       |         |         |           | populat |     |
|     |       |         |         |           | ion     |     |
|     |       |         |         |           | density |     |
|     |       |         |         |           | is      |     |
|     |       |         |         |           | unknown |     |
|     |       |         |         |           | ,       |     |
|     |       |         |         |           | set to  |     |
|     |       |         |         |           | -999.   |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 34  | O     | Traffic |         | Traffic   |         |     |
|     |       | Rate    |         | rate      |         |     |
|     |       |         |         | [veh km   |         |     |
|     |       |         |         | m-2       |         |     |
|     |       |         |         | s-1]      |         |     |
|     |       |         |         | Can be    |         |     |
|     |       |         |         | used      |         |     |
|     |       |         |         | for CO2   |         |     |
|     |       |         |         | flux      |         |     |
|     |       |         |         | calcula   |         |     |
|     |       |         |         | tion.     |         |     |
|     |       |         |         | **Do      |         |     |
|     |       |         |         | not use   |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | v2017a    |         |     |
|     |       |         |         | - set     |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | -999**    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 35  | O     | BuildEn |         | Buildin   |         |     |
|     |       | ergyUse |         | g         |         |     |
|     |       |         |         | energy    |         |     |
|     |       |         |         | use [W    |         |     |
|     |       |         |         | m-2]      |         |     |
|     |       |         |         | Can be    |         |     |
|     |       |         |         | used      |         |     |
|     |       |         |         | for CO2   |         |     |
|     |       |         |         | flux      |         |     |
|     |       |         |         | calcula   |         |     |
|     |       |         |         | tion.     |         |     |
|     |       |         |         | **Do      |         |     |
|     |       |         |         | not use   |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | v2017a    |         |     |
|     |       |         |         | - set     |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | -999**    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 36  | L     | Code_Pa | 331     | Code      |         |     |
|     |       | ved     |         | for       |         |     |
|     |       |         |         | Paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt,       |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | areas     |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt.       |         |     |
|     |       |         |         | e.g.      |         |     |
|     |       |         |         | 331       |         |     |
|     |       |         |         | means     |         |     |
|     |       |         |         | use the   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | row of    |         |     |
|     |       |         |         | input     |         |     |
|     |       |         |         | file      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt        |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | has 331   |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1         |         |     |
|     |       |         |         | (Code).   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 37  | L     | Code_Bl | 332     | Code      |         |     |
|     |       | dgs     |         | for       |         |     |
|     |       |         |         | Bldgs     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt,       |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | gs        |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt.       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 38  | L     | Code_Ev | 331     | Code      |         |     |
|     |       | eTr     |         | for       |         |     |
|     |       |         |         | EveTr     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_V   |         |     |
|     |       |         |         | eg.txt,   |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | evergre   |         |     |
|     |       |         |         | en        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | shrubs    |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_V   |         |     |
|     |       |         |         | eg.txt.   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 39  | L     | Code_De | 332     | Code      |         |     |
|     |       | cTr     |         | for       |         |     |
|     |       |         |         | DecTr     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_V   |         |     |
|     |       |         |         | eg.txt,   |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | deciduo   |         |     |
|     |       |         |         | us        |         |     |
|     |       |         |         | trees     |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | shrubs    |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_V   |         |     |
|     |       |         |         | eg.txt.   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 40  | L     | Code_Gr | 333     | Code      |         |     |
|     |       | ass     |         | for       |         |     |
|     |       |         |         | Grass     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_V   |         |     |
|     |       |         |         | eg.txt,   |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | grass     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_V   |         |     |
|     |       |         |         | eg.txt.   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 41  | L     | Code_Bs | 333     | Code      |         |     |
|     |       | oil     |         | for       |         |     |
|     |       |         |         | BSoil     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt,       |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | bare      |         |     |
|     |       |         |         | soil in   |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_N   |         |     |
|     |       |         |         | onVeg.t   |         |     |
|     |       |         |         | xt.       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 42  | L     | Code_Wa | 331     | Code      |         |     |
|     |       | ter     |         | for       |         |     |
|     |       |         |         | Water     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ater.tx   |         |     |
|     |       |         |         | t,        |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | open      |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ater.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 43  | MD    | LUMPS_D | 0.25    | Drainag   |         |     |
|     |       | rRate   |         | e         |         |     |
|     |       |         |         | rate of   |         |     |
|     |       |         |         | bucket    |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | LUMPS     |         |     |
|     |       |         |         | [mm       |         |     |
|     |       |         |         | h\ :sup   |         |     |
|     |       |         |         | :`-1`]    |         |     |
|     |       |         |         | Used      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | LUMPS     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | wetness   |         |     |
|     |       |         |         | control   |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | Default   |         |     |
|     |       |         |         | recomme   |         |     |
|     |       |         |         | nded      |         |     |
|     |       |         |         | value     |         |     |
|     |       |         |         | of 0.25   |         |     |
|     |       |         |         | mm        |         |     |
|     |       |         |         | h\ :sup   |         |     |
|     |       |         |         | :`-1`     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | Loridan   |         |     |
|     |       |         |         | et al.    |         |     |
|     |       |         |         | (2011)    |         |     |
|     |       |         |         | [L2011]_. |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 44  | MD    | LUMPS_C | 1       | Limit     |         |     |
|     |       | over    |         | when      |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | totally   |         |     |
|     |       |         |         | covered   |         |     |
|     |       |         |         | with      |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | [mm]      |         |     |
|     |       |         |         | Used      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | LUMPS     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | wetness   |         |     |
|     |       |         |         | control   |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | Default   |         |     |
|     |       |         |         | recomme   |         |     |
|     |       |         |         | nded      |         |     |
|     |       |         |         | value     |         |     |
|     |       |         |         | of 1 mm   |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | Loridan   |         |     |
|     |       |         |         | et al.    |         |     |
|     |       |         |         | (2011)    |         |     |
|     |       |         |         | [L2011]_. |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 45  | MD    | LUMPS_M | 10      | Maximum   |         |     |
|     |       | axRes   |         | water     |         |     |
|     |       |         |         | bucket    |         |     |
|     |       |         |         | reservo   |         |     |
|     |       |         |         | ir        |         |     |
|     |       |         |         | [mm]      |         |     |
|     |       |         |         | Used      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | LUMPS     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | wetness   |         |     |
|     |       |         |         | control   |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | Default   |         |     |
|     |       |         |         | recomme   |         |     |
|     |       |         |         | nded      |         |     |
|     |       |         |         | value     |         |     |
|     |       |         |         | of 10     |         |     |
|     |       |         |         | mm from   |         |     |
|     |       |         |         | Loridan   |         |     |
|     |       |         |         | et al.    |         |     |
|     |       |         |         | (2011)    |         |     |
|     |       |         |         | [L2011]_. |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 46  | MD    | NARP_Tr | 1       | Atmosph   |         |     |
|     |       | ans     |         | eric      |         |     |
|     |       |         |         | transmi   |         |     |
|     |       |         |         | ssivity   |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | NARP      |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | must in   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | range     |         |     |
|     |       |         |         | 0-1.      |         |     |
|     |       |         |         | Default   |         |     |
|     |       |         |         | recomme   |         |     |
|     |       |         |         | nded      |         |     |
|     |       |         |         | value     |         |     |
|     |       |         |         | of 1.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 47  | L     | CondCod | 33      | Code      |         |     |
|     |       | e       |         | for       |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | conduct   |         |     |
|     |       |         |         | ance      |         |     |
|     |       |         |         | paramet   |         |     |
|     |       |         |         | ers       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_C   |         |     |
|     |       |         |         | onducta   |         |     |
|     |       |         |         | nce.txt   |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | paramet   |         |     |
|     |       |         |         | ers       |         |     |
|     |       |         |         | for the   |         |     |
|     |       |         |         | Jarvis    |         |     |
|     |       |         |         | (1976)    |         |     |
|     |       |         |         | paramet   |         |     |
|     |       |         |         | erisati   |         |     |
|     |       |         |         | on        |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | conduct   |         |     |
|     |       |         |         | ance.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_C   |         |     |
|     |       |         |         | onducta   |         |     |
|     |       |         |         | nce.txt   |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | e.g. 33   |         |     |
|     |       |         |         | means     |         |     |
|     |       |         |         | use the   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | row of    |         |     |
|     |       |         |         | input     |         |     |
|     |       |         |         | file      |         |     |
|     |       |         |         | SUEWS_C   |         |     |
|     |       |         |         | onducta   |         |     |
|     |       |         |         | nce.txt   |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | has 33    |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1         |         |     |
|     |       |         |         | (Code).   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 48  | L     | SnowCod | 33      | Code      |         |     |
|     |       | e       |         | for       |         |     |
|     |       |         |         | snow      |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_S   |         |     |
|     |       |         |         | now.txt   |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | contain   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | attribu   |         |     |
|     |       |         |         | tes       |         |     |
|     |       |         |         | describ   |         |     |
|     |       |         |         | ing       |         |     |
|     |       |         |         | snow      |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in this   |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | this      |         |     |
|     |       |         |         | year.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_S   |         |     |
|     |       |         |         | now.txt   |         |     |
|     |       |         |         | .         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 49  | L     | SnowCle | 1       | Code      |         |     |
|     |       | aringPr |         | for       |         |     |
|     |       | ofWD    |         | snow      |         |     |
|     |       |         |         | clearin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (weekda   |         |     |
|     |       |         |         | ys)       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | e.g. 1    |         |     |
|     |       |         |         | means     |         |     |
|     |       |         |         | use the   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | row of    |         |     |
|     |       |         |         | input     |         |     |
|     |       |         |         | file      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt      |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | has 1     |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1         |         |     |
|     |       |         |         | (Code).   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 50  | L     | SnowCle | 1       | Code      |         |     |
|     |       | aringPr |         | for       |         |     |
|     |       | ofWE    |         | snow      |         |     |
|     |       |         |         | clearin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (weeken   |         |     |
|     |       |         |         | ds)       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | e.g. 1    |         |     |
|     |       |         |         | means     |         |     |
|     |       |         |         | use the   |         |     |
|     |       |         |         | charact   |         |     |
|     |       |         |         | eristic   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | row of    |         |     |
|     |       |         |         | input     |         |     |
|     |       |         |         | file      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt      |         |     |
|     |       |         |         | which     |         |     |
|     |       |         |         | has 1     |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1         |         |     |
|     |       |         |         | (Code).   |         |     |
|     |       |         |         | Providi   |         |     |
|     |       |         |         | ng        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | same      |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | SnowCle   |         |     |
|     |       |         |         | aringPr   |         |     |
|     |       |         |         | ofWD      |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | SnowCle   |         |     |
|     |       |         |         | aringPr   |         |     |
|     |       |         |         | ofWE      |         |     |
|     |       |         |         | would     |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | same      |         |     |
|     |       |         |         | row in    |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt,     |         |     |
|     |       |         |         | i.e.      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | same      |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | would     |         |     |
|     |       |         |         | be used   |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | weekday   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | weekend   |         |     |
|     |       |         |         | s.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 51  | L     | Anthrop | 33      | Code      | RunCont |     |
|     |       | ogenicC |         | for       | rol.nml |     |
|     |       | ode     |         | modelli   | ]]).    |     |
|     |       |         |         | ng        | Value   |     |
|     |       |         |         | anthrop   | of      |     |
|     |       |         |         | ogenic    | integer |     |
|     |       |         |         | heat      | is      |     |
|     |       |         |         | flux      | arbitra |     |
|     |       |         |         | Provide   | ry      |     |
|     |       |         |         | s         | but     |     |
|     |       |         |         | the       | must    |     |
|     |       |         |         | link to   | match   |     |
|     |       |         |         | column    | code    |     |
|     |       |         |         | 1 of      | specifi |     |
|     |       |         |         | SUEWS_A   | ed      |     |
|     |       |         |         | nthropo   | in      |     |
|     |       |         |         | genicHe   | column  |     |
|     |       |         |         | at.txt,   | 1 of    |     |
|     |       |         |         | which     | SUEWS_A |     |
|     |       |         |         | contain   | nthropo |     |
|     |       |         |         | s         | genicHe |     |
|     |       |         |         | the       | at.txt. |     |
|     |       |         |         | model     |         |     |
|     |       |         |         | coeffic   |         |     |
|     |       |         |         | ients     |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | estimat   |         |     |
|     |       |         |         | ion       |         |     |
|     |       |         |         | of the    |         |     |
|     |       |         |         | anthrop   |         |     |
|     |       |         |         | ogenic    |         |     |
|     |       |         |         | heat      |         |     |
|     |       |         |         | flux      |         |     |
|     |       |         |         | (used     |         |     |
|     |       |         |         | if        |         |     |
|     |       |         |         | Anthrop   |         |     |
|     |       |         |         | HeatCho   |         |     |
|     |       |         |         | ice       |         |     |
|     |       |         |         | = 1, 2    |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | [[#RunC   |         |     |
|     |       |         |         | ontrol.   |         |     |
|     |       |         |         | nml       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 52  | L     | EnergyU | 333     | Code      |         |     |
|     |       | seProfW |         | for       |         |     |
|     |       | D       |         | energy    |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (weekda   |         |     |
|     |       |         |         | ys)       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Look      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | codes     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 53  | L     | EnergyU | 334     | Code      |         |     |
|     |       | seProfW |         | for       |         |     |
|     |       | E       |         | energy    |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (weeken   |         |     |
|     |       |         |         | ds)       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 54  | L     | Activit | 333     | Code      |         |     |
|     |       | yProfWD |         | for       |         |     |
|     |       |         |         | human     |         |     |
|     |       |         |         | activit   |         |     |
|     |       |         |         | y         |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (weekda   |         |     |
|     |       |         |         | ys)       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Look      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | codes     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Used      |         |     |
|     |       |         |         | for CO2   |         |     |
|     |       |         |         | flux      |         |     |
|     |       |         |         | calcula   |         |     |
|     |       |         |         | tion      |         |     |
|     |       |         |         | - **not   |         |     |
|     |       |         |         | used in   |         |     |
|     |       |         |         | v2017a*   |         |     |
|     |       |         |         | *         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 55  | L     | Activit | 333     | Code      |         |     |
|     |       | yProfWE |         | for       |         |     |
|     |       |         |         | human     |         |     |
|     |       |         |         | activit   |         |     |
|     |       |         |         | y         |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (weeken   |         |     |
|     |       |         |         | ds)       |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Look      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | codes     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Used      |         |     |
|     |       |         |         | for CO2   |         |     |
|     |       |         |         | flux      |         |     |
|     |       |         |         | calcula   |         |     |
|     |       |         |         | tion      |         |     |
|     |       |         |         | - **not   |         |     |
|     |       |         |         | used in   |         |     |
|     |       |         |         | v2017a*   |         |     |
|     |       |         |         | *         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 56  | L     | Irrigat | 33      | Code      | RunCont |     |
|     |       | ionCode |         | for       | rol.nml |     |
|     |       |         |         | modelli   | ]]).    |     |
|     |       |         |         | ng        | Value   |     |
|     |       |         |         | irrigat   | of      |     |
|     |       |         |         | ion       | integer |     |
|     |       |         |         | Provide   | is      |     |
|     |       |         |         | s         | arbitra |     |
|     |       |         |         | the       | ry      |     |
|     |       |         |         | link to   | but     |     |
|     |       |         |         | column    | must    |     |
|     |       |         |         | 1 of      | match   |     |
|     |       |         |         | SUEWS_I   | code    |     |
|     |       |         |         | rrigati   | specifi |     |
|     |       |         |         | on.txt,   | ed      |     |
|     |       |         |         | which     | in      |     |
|     |       |         |         | contain   | column  |     |
|     |       |         |         | s         | 1 of    |     |
|     |       |         |         | the       | SUEWS_I |     |
|     |       |         |         | model     | rrigati |     |
|     |       |         |         | coeffic   | on.txt. |     |
|     |       |         |         | ients     |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | estimat   |         |     |
|     |       |         |         | ion       |         |     |
|     |       |         |         | of the    |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | (used     |         |     |
|     |       |         |         | if        |         |     |
|     |       |         |         | WU_Choi   |         |     |
|     |       |         |         | ce        |         |     |
|     |       |         |         | = 0 in    |         |     |
|     |       |         |         | [[#RunC   |         |     |
|     |       |         |         | ontrol.   |         |     |
|     |       |         |         | nml       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 57  | L     | WaterUs | 335     | Code      |         |     |
|     |       | eProfMa |         | for       |         |     |
|     |       | nuWD    |         | water     |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (manual   |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ion,      |         |     |
|     |       |         |         | weekday   |         |     |
|     |       |         |         | s)        |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 58  | L     | WaterUs | 336     | Code      |         |     |
|     |       | eProfMa |         | for       |         |     |
|     |       | nuWE    |         | water     |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (manual   |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ion,      |         |     |
|     |       |         |         | weekend   |         |     |
|     |       |         |         | s)        |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 59  | L     | WaterUs | 337     | Code      |         |     |
|     |       | eProfAu |         | for       |         |     |
|     |       | toWD    |         | water     |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (automa   |         |     |
|     |       |         |         | tic       |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ion,      |         |     |
|     |       |         |         | weekday   |         |     |
|     |       |         |         | s)        |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 60  | L     | WaterUs | 338     | Code      |         |     |
|     |       | eProfAu |         | for       |         |     |
|     |       | toWE    |         | water     |         |     |
|     |       |         |         | use       |         |     |
|     |       |         |         | profile   |         |     |
|     |       |         |         | (automa   |         |     |
|     |       |         |         | tic       |         |     |
|     |       |         |         | irrigat   |         |     |
|     |       |         |         | ion,      |         |     |
|     |       |         |         | weekend   |         |     |
|     |       |         |         | s)        |         |     |
|     |       |         |         | Provide   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | link to   |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_P   |         |     |
|     |       |         |         | rofiles   |         |     |
|     |       |         |         | .txt.     |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 61  | MD    | FlowCha | 0       | Differe   | '''     |     |
|     |       | nge     |         | nce       |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | input     |         |     |
|     |       |         |         | and       |         |     |
|     |       |         |         | output    |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | [mm       |         |     |
|     |       |         |         | h\ :sup   |         |     |
|     |       |         |         | :`-1`]    |         |     |
|     |       |         |         | Used to   |         |     |
|     |       |         |         | indicat   |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | river     |         |     |
|     |       |         |         | or        |         |     |
|     |       |         |         | stream    |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | through   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid.     |         |     |
|     |       |         |         | '''Curr   |         |     |
|     |       |         |         | ently     |         |     |
|     |       |         |         | not       |         |     |
|     |       |         |         | fully     |         |     |
|     |       |         |         | tested    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 62  | MD,MU | RunoffT | 0.1     | Fractio   |         |     |
|     |       | oWater  |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | above-g   |         |     |
|     |       |         |         | round     |         |     |
|     |       |         |         | runoff    |         |     |
|     |       |         |         | flowing   |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | during    |         |     |
|     |       |         |         | floodin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | [-]       |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | must be   |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | range     |         |     |
|     |       |         |         | 0-1.      |         |     |
|     |       |         |         | Fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | above-g   |         |     |
|     |       |         |         | round     |         |     |
|     |       |         |         | runoff    |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | in the    |         |     |
|     |       |         |         | case of   |         |     |
|     |       |         |         | floodin   |         |     |
|     |       |         |         | g.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 63  | MD,MU | PipeCap | 100     | Storage   |         |     |
|     |       | acity   |         | capacit   |         |     |
|     |       |         |         | y         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | pipes     |         |     |
|     |       |         |         | [mm]      |         |     |
|     |       |         |         | Runoff    |         |     |
|     |       |         |         | amounti   |         |     |
|     |       |         |         | ng        |         |     |
|     |       |         |         | to less   |         |     |
|     |       |         |         | than      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | value     |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | here is   |         |     |
|     |       |         |         | assumed   |         |     |
|     |       |         |         | to be     |         |     |
|     |       |         |         | removed   |         |     |
|     |       |         |         | by        |         |     |
|     |       |         |         | pipes.    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 64  | MD,MU | GridCon | 2       | Number    | Grid    | ''' |
|     |       | nection |         | of the    | Connect |     |
|     |       | 1of8    |         | grid      | ions]]  |     |
|     |       |         |         | where     | '''Not  |     |
|     |       |         |         | water     | current |     |
|     |       |         |         | can       | ly      |     |
|     |       |         |         | flow to   | impleme |     |
|     |       |         |         | [-]       | nted    |     |
|     |       |         |         | -  The    |         |     |
|     |       |         |         | next      |         |     |
|     |       |         |         | 8         |         |     |
|     |       |         |         | pair      |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | colu      |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | spec      |         |     |
|     |       |         |         | ify       |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s.        |         |     |
|     |       |         |         | -  The    |         |     |
|     |       |         |         | firs      |         |     |
|     |       |         |         | t         |         |     |
|     |       |         |         | colu      |         |     |
|     |       |         |         | mn        |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | each      |         |     |
|     |       |         |         | pair      |         |     |
|     |       |         |         | spec      |         |     |
|     |       |         |         | ifies     |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | (fro      |         |     |
|     |       |         |         | m         |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | curr      |         |     |
|     |       |         |         | ent       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | colu      |         |     |
|     |       |         |         | mn        |         |     |
|     |       |         |         | 1);       |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | seco      |         |     |
|     |       |         |         | nd        |         |     |
|     |       |         |         | colu      |         |     |
|     |       |         |         | mn        |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | each      |         |     |
|     |       |         |         | pair      |         |     |
|     |       |         |         | spec      |         |     |
|     |       |         |         | ifies     |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | frac      |         |     |
|     |       |         |         | tion      |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | -  The    |         |     |
|     |       |         |         | frac      |         |     |
|     |       |         |         | tion      |         |     |
|     |       |         |         | (i.e      |         |     |
|     |       |         |         | .         |         |     |
|     |       |         |         | amou      |         |     |
|     |       |         |         | nt)       |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | tran      |         |     |
|     |       |         |         | sferred   |         |     |
|     |       |         |         | may       |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | esti      |         |     |
|     |       |         |         | mated     |         |     |
|     |       |         |         | base      |         |     |
|     |       |         |         | d         |         |     |
|     |       |         |         | on        |         |     |
|     |       |         |         | elev      |         |     |
|     |       |         |         | ation,    |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | leng      |         |     |
|     |       |         |         | th        |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | conn      |         |     |
|     |       |         |         | ecting    |         |     |
|     |       |         |         | surf      |         |     |
|     |       |         |         | ace       |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s,        |         |     |
|     |       |         |         | pres      |         |     |
|     |       |         |         | ence      |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | wall      |         |     |
|     |       |         |         | s,        |         |     |
|     |       |         |         | etc.      |         |     |
|     |       |         |         | -  Wate   |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | cann      |         |     |
|     |       |         |         | ot        |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | curr      |         |     |
|     |       |         |         | ent       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | same      |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | ,         |         |     |
|     |       |         |         | so        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | numb      |         |     |
|     |       |         |         | er        |         |     |
|     |       |         |         | here      |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | be        |         |     |
|     |       |         |         | diff      |         |     |
|     |       |         |         | erent     |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | numb      |         |     |
|     |       |         |         | er        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | colu      |         |     |
|     |       |         |         | mn        |         |     |
|     |       |         |         | 1.        |         |     |
|     |       |         |         | Wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | to a      |         |     |
|     |       |         |         | maxi      |         |     |
|     |       |         |         | mum       |         |     |
|     |       |         |         | of 8      |         |     |
|     |       |         |         | othe      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s.        |         |     |
|     |       |         |         | -  If     |         |     |
|     |       |         |         | ther      |         |     |
|     |       |         |         | e         |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | no        |         |     |
|     |       |         |         | wate      |         |     |
|     |       |         |         | r         |         |     |
|     |       |         |         | flow      |         |     |
|     |       |         |         | betw      |         |     |
|     |       |         |         | een       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | s,        |         |     |
|     |       |         |         | or a      |         |     |
|     |       |         |         | sing      |         |     |
|     |       |         |         | le        |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | run,      |         |     |
|     |       |         |         | set       |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | 0.        |         |     |
|     |       |         |         | \*See     |         |     |
|     |       |         |         | section   |         |     |
|     |       |         |         | on        |         |     |
|     |       |         |         | [[#Grid   |         |     |
|     |       |         |         | Connect   |         |     |
|     |       |         |         | ions      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 65  | MD,MU | Fractio | 0.2     | Fractio   |         |     |
|     |       | n1of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 66  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 2of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 67  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n2of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 68  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 3of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 69  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n3of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 70  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 4of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 71  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n4of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 72  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 5of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 73  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n5of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 74  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 6of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 75  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n6of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 76  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 7of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 77  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n7of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 78  | MD,MU | GridCon | 0       | Number    |         |     |
|     |       | nection |         | of the    |         |     |
|     |       | 8of8    |         | grid      |         |     |
|     |       |         |         | where     |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 79  | MD,MU | Fractio | 0       | Fractio   |         |     |
|     |       | n8of8   |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | can       |         |     |
|     |       |         |         | flow to   |         |     |
|     |       |         |         | the       |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | previou   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | [-]       |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 80  | L     | WithinG | 331     | Code      | SUEWS_W |     |
|     |       | ridPave |         | that      | ithinGr |     |
|     |       | dCode   |         | links     | idWater |     |
|     |       |         |         | to the    | Dist.tx |     |
|     |       |         |         | fractio   | t]].    |     |
|     |       |         |         | n         | Value   |     |
|     |       |         |         | of        | of      |     |
|     |       |         |         | water     | integer |     |
|     |       |         |         | that      | is      |     |
|     |       |         |         | flows     | arbitra |     |
|     |       |         |         | from      | ry      |     |
|     |       |         |         | Paved     | but     |     |
|     |       |         |         | surface   | must    |     |
|     |       |         |         | s         | match   |     |
|     |       |         |         | to        | code    |     |
|     |       |         |         | surface   | specifi |     |
|     |       |         |         | s         | ed      |     |
|     |       |         |         | in        | in      |     |
|     |       |         |         | columns   | column  |     |
|     |       |         |         | 2-10 of   | 1 of    |     |
|     |       |         |         | [[#SUEW   | SUEWS_W |     |
|     |       |         |         | S_Withi   | ithinGr |     |
|     |       |         |         | nGridWa   | idWater |     |
|     |       |         |         | terDist   | Dist.tx |     |
|     |       |         |         | .txt      | t.      |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 81  | L     | WithinG | 332     | Code      |         |     |
|     |       | ridBldg |         | that      |         |     |
|     |       | sCode   |         | links     |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | Bldgs     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | columns   |         |     |
|     |       |         |         | 2-10 of   |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 82  | L     | WithinG | 333     | Code      |         |     |
|     |       | ridEveT |         | that      |         |     |
|     |       | rCode   |         | links     |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | EveTr     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | columns   |         |     |
|     |       |         |         | 2-10 of   |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 83  | L     | WithinG | 334     | Code      |         |     |
|     |       | ridDecT |         | that      |         |     |
|     |       | rCode   |         | links     |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | DecTr     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | columns   |         |     |
|     |       |         |         | 2-10 of   |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 84  | L     | WithinG | 335     | Code      |         |     |
|     |       | ridGras |         | that      |         |     |
|     |       | sCode   |         | links     |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | Grass     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | columns   |         |     |
|     |       |         |         | 2-10 of   |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 85  | L     | WithinG | 336     | Code      |         |     |
|     |       | ridBSoi |         | that      |         |     |
|     |       | lCode   |         | links     |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | BSoil     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | columns   |         |     |
|     |       |         |         | 2-10 of   |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 86  | L     | WithinG | 337     | Code      |         |     |
|     |       | ridWate |         | that      |         |     |
|     |       | rCode   |         | links     |         |     |
|     |       |         |         | to the    |         |     |
|     |       |         |         | fractio   |         |     |
|     |       |         |         | n         |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | water     |         |     |
|     |       |         |         | that      |         |     |
|     |       |         |         | flows     |         |     |
|     |       |         |         | from      |         |     |
|     |       |         |         | Water     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | to        |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | s         |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | columns   |         |     |
|     |       |         |         | 2-10 of   |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
|     |       |         |         | Value     |         |     |
|     |       |         |         | of        |         |     |
|     |       |         |         | integer   |         |     |
|     |       |         |         | is        |         |     |
|     |       |         |         | arbitra   |         |     |
|     |       |         |         | ry        |         |     |
|     |       |         |         | but       |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | match     |         |     |
|     |       |         |         | code      |         |     |
|     |       |         |         | specifi   |         |     |
|     |       |         |         | ed        |         |     |
|     |       |         |         | in        |         |     |
|     |       |         |         | column    |         |     |
|     |       |         |         | 1 of      |         |     |
|     |       |         |         | SUEWS_W   |         |     |
|     |       |         |         | ithinGr   |         |     |
|     |       |         |         | idWater   |         |     |
|     |       |         |         | Dist.tx   |         |     |
|     |       |         |         | t.        |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 87  | MU    | AreaWal | 1.08    | Area of   |         |     |
|     |       | l       |         | wall      |         |     |
|     |       |         |         | within    |         |     |
|     |       |         |         | grid      |         |     |
|     |       |         |         | (needed   |         |     |
|     |       |         |         | for       |         |     |
|     |       |         |         | ESTM      |         |     |
|     |       |         |         | calcula   |         |     |
|     |       |         |         | tion).    |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 88  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_P |         | n         |         |     |
|     |       | aved1   |         | of        |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 1   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 88-9      |         |     |
|     |       |         |         | 0         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 89  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_P |         | n         |         |     |
|     |       | aved2   |         | of        |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 2   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 88-9      |         |     |
|     |       |         |         | 0         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 90  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_P |         | n         |         |     |
|     |       | aved3   |         | of        |         |     |
|     |       |         |         | paved     |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 3   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 88-9      |         |     |
|     |       |         |         | 0         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 91  | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Paved1 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 92  | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Paved2 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 93  | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Paved3 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 94  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_B |         | n         |         |     |
|     |       | ldgs1   |         | of        |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 1   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 94-9      |         |     |
|     |       |         |         | 8         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 95  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_B |         | n         |         |     |
|     |       | ldgs2   |         | of        |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 2   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 94-9      |         |     |
|     |       |         |         | 8         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 96  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_B |         | n         |         |     |
|     |       | ldgs3   |         | of        |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 3   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 94-9      |         |     |
|     |       |         |         | 8         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 97  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_B |         | n         |         |     |
|     |       | ldgs4   |         | of        |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 4   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 94-9      |         |     |
|     |       |         |         | 8         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 98  | MU    | Fr_ESTM |         | Fractio   |         |     |
|     |       | Class_B |         | n         |         |     |
|     |       | ldgs5   |         | of        |         |     |
|     |       |         |         | buildin   |         |     |
|     |       |         |         | g         |         |     |
|     |       |         |         | surface   |         |     |
|     |       |         |         | classif   |         |     |
|     |       |         |         | ied       |         |     |
|     |       |         |         | as ESTM   |         |     |
|     |       |         |         | class 5   |         |     |
|     |       |         |         | -  Colu   |         |     |
|     |       |         |         | mns       |         |     |
|     |       |         |         | 94-9      |         |     |
|     |       |         |         | 8         |         |     |
|     |       |         |         | must      |         |     |
|     |       |         |         | add       |         |     |
|     |       |         |         | up        |         |     |
|     |       |         |         | to 1      |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 99  | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Bldgs1 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 100 | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Bldgs2 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 101 | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Bldgs3 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 102 | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Bldgs4 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
| 103 | L     | Code_ES |         | Code      | SUEWS_E |     |
|     |       | TMClass |         | linking   | STMCoef |     |
|     |       | _Bldgs5 |         | to        | ficient |     |
|     |       |         |         | [[#SUEW   | s.txt]] |     |
|     |       |         |         | S_ESTMC   |         |     |
|     |       |         |         | oeffici   |         |     |
|     |       |         |         | ents.tx   |         |     |
|     |       |         |         | t         |         |     |
+-----+-------+---------+---------+-----------+---------+-----+
|     |       |         |         |           |         |     |
+-----+-------+---------+---------+-----------+---------+-----+

Day Light Savings (DLS)
^^^^^^^^^^^^^^^^^^^^^^^

The dates for DLS normally vary each year and country as they are often
associated with a specific set of Sunday mornings at the beginning of
summer and autumn. Note it is important to remember leap years. You can
check http://www.timeanddate.com/time/dst/ for your city.

If DLS does not occur give a start and end day immediately after it.
Make certain the dummy dates are correct for the hemisphere:

| ``for northern hemisphere, use: 180 181``
| ``for southern hemisphere, use:  365 1``

+----------------+------+----------+-----------------+
| Example:       | Year | start of | end of daylight |
|                |      | daylight | savings         |
|                |      | savings  |                 |
+================+======+==========+=================+
| when running   | 2008 | 170      | 240             |
| multiple years |      |          |                 |
| (in this case  |      |          |                 |
| 2008 and 2009  |      |          |                 |
| in Canada)     |      |          |                 |
+----------------+------+----------+-----------------+
|                | 2009 | 172      | 242             |
+----------------+------+----------+-----------------+
|                |      |          |                 |
+----------------+------+----------+-----------------+


Grid Connections (water flow between grids)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**N.B. not currently implemented** - columns 64-79 of
`SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__ can be set to zero.

This section gives an example of water flow between grids, calculated
based on the relative elevation of the grids and length of the
connecting surface between adjacent grids. For the square grids in the
figure, water flow is assumed to be zero between diagonally adjacent
grids, as the length of connecting surface linking the grids is very
small. Model grids need not be square or the same size.

The table gives example values for the grid connections part of
`SUEWS_SiteSelect.txt <#SUEWS_SiteSelect.txt>`__ for the grids shown in
the figure. For each row, only water flowing out of the current grid is
entered (e.g. water flows from 234 to 236 and 237, with a larger
proportion of water flowing to 237 because of the greater length of
connecting surface between 234 and 237 than between 234 and 236. No
water is assumed to flow between 234 and 233 or 235 because there is no
elevation difference between these grids. Grids 234 and 238 are at the
same elevation and only connect at a point, so no water flows between
them. Water enters grid 234 from grids 230, 231 and 232 as these are
more elevated.

[[File:GridConnections_1.jpg%7Cframe\ \|

``Example grid connections showing water flow between grids. Arrows indicate the water flow in to and out of grid 234, but note that only only water flowing out of each grid is entered in SUEWS_SiteSelect.txt.|none]]``

.. figure:: GridConnections_2_v2.jpg
   :alt:  Example values for the grid connections part of SUEWS_SiteSelect.txt for the grids.|none