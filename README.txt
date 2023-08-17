UW-BioNLP Clinical Record Section Chunker
Section Annotations for i2b2 De-identified Discharge Summaries

Author: Weipeng Zhou <wzhou87@uw.edu>
Date: 8/11/2023
*************************************************************
The section header texts in the annotations are removed and the resulted annotations are released to the public. Only instances of the spans are provided.

Author: Prescott Klassen <klassp@uw.edu>
Date: 12/2/2013 
*************************************************************

The BRAT directory contains a five fold collection of annotation for 183 randomly selected 
i2b2 discharge summaries (https://i2b2.org/NLP/DataSets/) annotated using the BRAT 
annotation tool(http://brat.nlplab.org/) and a simple Section Header annotation schema.

The files on which the annotations were based, were selected from the 2010 i2b2 Discharge 
Summary corpus created for the 2010 i2b2 natural language processing challenge on medical 
concept, assertion, and relation extraction. The corpus consists of 835 discharge 
summaries from 3 institutions (Partners HeathCare, Beth Israel Deaconess Medical Center, 
and University of Pittsburgh Medical Center). See (Uzuner, et al, 2011) for more detail:

Ozlem Uzuner, Brett R. South, Shuying Shen, and Scott L. Duvall. 2011. 2010 i2b2/VA 
    challenge on concepts, assertions, and relations in clinical text. Journal of the
    American Medical Informatics Association, 18:552–556.

183 discharge summaries were selected for annotation and used to develop and test the 
UW-BioNLP Clinical Record Section Chunker. The files were annotated using a 
simple schema for section headings in the GATE annotation tool (http://gate.ac.uk/). 
See (Tepper, et al, 2012) for more detail:

M. Tepper, D. Capurro, F. Xia, L. Vanderwende, M. Yetisgen-Yildiz. Statistical Section 
    Segmentation in Free-Text Clinical Records. Proceedings of the International 
    Conference on Language Resources and Evaluation (LREC), Istanbul, May, 2012.

    http://www.lrec-conf.org/proceedings/lrec2012/pdf/1016_Paper.pdf
    
The collection of 183 BRAT annotation files were automatically converted 
from the GATE XML format to BRAT .ann format. The BRAT annotation files are stand-off 
markup and are separate from the original text files.

If you have a license for the original i2b2 files from the 2010 i2b2 Discharge Summary
corpus, you can simply copy the files into the directory structure of this collection. At 
the end of this README.txt is a list of files in the collection, and 5 bash array 
declarations containing the randomly sequenced test folds. In order to use the files with 
the UW-BioNLP Clinical Record Section Chunker the .txt files (original source) must have 
the same name and be placed in the same directory as the .ann (BRAT annotation files).

BRAT Schema and configuration files
************************************

In order to edit the .ann files in this collection or create new files annotated with the
UW-BioNLP Clinical Record Section Chunker Section schema, three configuration files are 
provided in the directory schema_artifacts.

annotation.conf                   annotation schema
visual.conf                       visual styles
tools.conf                        editor settings

GATE Schema
***********

The original GATE documents are based on a simple schema of a 'Section Header' 
Annotation element with a single Feature child element which contains a Name and Value 
child element. See below for an example instance of the schema applied in GATE.

<Annotation Id="1" Type="Section Header" StartNode="333" EndNode="356">
<Feature>
  <Name className="java.lang.String">type</Name>
  <Value className="java.lang.String">Discharge Date</Value>
</Feature>

The UW-BioNLP Clinical Record Section Chunker Section will process XML files exported 
from GATE with Section Header Annotation elements.

List of i2b2 Discharge Summary files:
************************************

020501989_DH
042335965_SC
057594022_DH
081039790_EH
134300717
143748600 SC
163688755
168484101
172352273_WGH
173436079
197872734_YC
245317863_WGH
262473207
269463740
284487129
288506174_ELMVH
305265793_a
305265793_c
305265793_d
306968218_YC
308353658_PUMC
323541974_PUMC
331144840
332803550
333084519
337483886
342570083
373254497_PUMC
397500866_SC
420033129_YC
430403085_SC
442434998
454860720_WGH
458711317
463067067
476664819_RWH
506243692_c
511454195
517414339
517502848_ELMVH
536196468
559197012_c
578255201_EH
684476505_WGH
694420471_WGH
701572223
702031153_YC
714007792_SC
718477487
719127931
721206493
723989226
745431641_WGH
745701560_WGH
782673825
788268693_DH
807558580_EH
819380356_ELMVH
825330116
827228650_YC
829426955_DH
831471289
848649595_SC
851842962
853434910
869436718_SC
879492218_YC
884948991
886778915_WGH
910458031
914783811
931376689_ELMVH
935669761_PUMC
974628880_YC
979440029_RWH
discharge0
discharge1
discharge101
discharge106
discharge110
discharge115
discharge118
discharge15
discharge18
discharge19
discharge202
discharge207
discharge209
discharge217
discharge233
discharge237
discharge240
discharge241
discharge242
discharge253
discharge259
discharge26
discharge261
discharge264
discharge266
discharge268
discharge270
discharge272
discharge285
discharge29
discharge295
discharge308
discharge310
discharge316
discharge319
discharge320
discharge325
discharge332
discharge34
discharge343
discharge346
discharge350
discharge353
discharge354
discharge356
discharge37
discharge375
discharge379
discharge382
discharge388
discharge392
discharge399
discharge400
discharge402
discharge406
discharge411
discharge413
discharge416
discharge417
discharge430
discharge433
discharge436
discharge443
discharge444
discharge447
discharge449
discharge453
discharge454
discharge458
discharge469
discharge472
discharge477
discharge478
discharge489
discharge491
discharge494
discharge496
discharge51
discharge53
discharge59
discharge72
discharge77
discharge83
discharge84
discharge88
discharge98
discharge99
record-105
record-107
record-109
record-122
record-140
record-143
record-144
record-15
record-175
record-178
record-18
record-26
record-29
record-36
record-45
record-48
record-51
record-59
record-66
record-83
record-84

Test folds for 5 Fold Cross-Evaluation
***************************************

# Bash arrays of test folds for 5-fold cross-evaluation

RAND_0_ARRAY=('305265793_d' 'record-15' '373254497_PUMC' '511454195' '714007792_SC' 
              '476664819_RWH' 'discharge449' 'discharge207' 'record-59' '020501989_DH' 
              'discharge84' '745701560_WGH' '081039790_EH' '719127931' 'record-143' 
              'discharge379' 'record-51' 'discharge388' '168484101' 'discharge320' 
              'discharge217' 'record-48' 'discharge98' '974628880_YC' 'discharge343' 
              'record-105' 'discharge447' '869436718_SC' 'discharge406' '269463740' 
              '042335965_SC' 'discharge83' '323541974_PUMC' '536196468' 'discharge268' 
              '332803550' 'discharge472')

RAND_1_ARRAY=('record-18' 'discharge270' '342570083' '288506174_ELMVH' '931376689_ELMVH' 
              '819380356_ELMVH' 'discharge489' 'discharge1' 'discharge106' 'discharge454' 
              'record-83' 'discharge350' '979440029_RWH' '463067067' 'record-29' 
              '454860720_WGH' 'record-178' '331144840' '517502848_ELMVH' 'discharge253' 
              '718477487' '163688755' 'discharge478' '173436079' '057594022_DH' 
              'discharge346' 'discharge356' 'discharge53' '831471289' 'discharge272' 
              'discharge19' '723989226' '702031153_YC' 'discharge444' '788268693_DH' 
              '694420471_WGH' 'record-122')

RAND_2_ARRAY=('discharge319' 'discharge399' '134300717' 'discharge353' 'discharge458' 
              'discharge436' 'discharge26' 'record-84' 'discharge72' 'discharge295' 
              'discharge413' 'discharge261' '827228650_YC' '829426955_DH' 'discharge209' 
              'discharge453' '578255201_EH' '684476505_WGH' '397500866_SC' 'discharge241' 
              '825330116' 'discharge400' 'discharge264' 'discharge375' 'discharge325' 
              'discharge110' 'record-175' '308353658_PUMC' 'discharge51' '305265793_a' 
              '442434998' 'discharge59' '721206493' 'discharge496' '853434910' 
              'discharge332' '886778915_WGH')

RAND_3_ARRAY=('discharge37' '701572223' '305265793_c' 'record-36' 'discharge99' 
              'discharge310' '914783811' 'discharge240' '143748600_SC' 'discharge417' 
              'discharge29' '284487129' 'discharge494' 'discharge118' '848649595_SC' 
              'discharge18' '517414339' 'record-66' '337483886' 'discharge34' 
              '935669761_PUMC' 'record-109' '306968218_YC' '910458031' '458711317' 
              '851842962' '420033129_YC' 'discharge491' 'discharge266' 'discharge233' 
              '172352273_WGH' 'discharge354' '430403085_SC' 'discharge443' 'discharge308' 
              'record-26')

RAND_4_ARRAY=('discharge15' '333084519' 'discharge433' '245317863_WGH' '782673825' 
              'record-140' 'discharge430' 'discharge416' '506243692_c' 'discharge477' 
              '262473207' 'discharge77' 'record-45' 'discharge237' 'discharge411' 
              '807558580_EH' 'discharge242' 'discharge101' 'record-144' '559197012_c' 
              'discharge392' 'discharge259' '197872734_YC' 'discharge382' '884948991' 
              'discharge88' 'discharge402' '745431641_WGH' 'discharge115' 'discharge285' 
              'discharge202' 'discharge0' 'record-107' 'discharge316' 'discharge469' 
              '879492218_YC')
 
 




