# DFATPL--Dataset for "Empirical study on developer factors affecting tossing path length of bug reports"

## References

If you use our dataset or code, please cite [our paper](http://digital-library.theiet.org/content/journals/10.1049/iet-sen.2017.0159):

```
@inproceedings{fmow2018,
  title={Empirical study on developer factors affecting tossing path length of bug reports},
  author={Hongrun Wu, Haiyang Liu, Yutao Ma},
  journal={IET Software},
  volume={12},
  number={3},
  pages={258–270},
  year={2018},
}
```

## Data description

DFATPL_Eclipse contains two files "history&tp" and "input_data", which are the datasets for experiments of Eclipse project in the paper. The file DFATPL_Mozilla contains the data used for experiments of Mozilla project.

```
1. history&tp -- the history and tossing path of 200000 bug reports for Eclipse project.

(a) Bughistory_filter -- This dataset contains the changing history ("When", "Who", "What", "Added", "Removed") of a bug report. This dataset is filtered from "Bughistory.rar" by exacting the "What" filed with "Assignee", "Status" and "Resolution".  
Data details of BugID 35:
When	 	 	 	 	 Who	 	 	 	 What	 	 	 Added	 	 	 Removed
2001-10-12 16:36:59 EDT	jean-michel_lemieux	Assignee	Michael_Valenta	Jean-Michel_Lemieux
2001-10-12 16:36:59 EDT	jean-michel_lemieux	Status	NEW	ASSIGNED
2001-10-18 16:21:36 EDT	Michael_Valenta	Status	ASSIGNED	NEW
2002-03-27 11:29:44 EST	Michael_Valenta	Assignee	Jean-Michel_Lemieux	Michael_Valenta
2002-03-27 11:29:44 EST	Michael_Valenta	Status	NEW	ASSIGNED
2002-03-27 11:29:44 EST	Michael_Valenta	Status	NEW	ASSIGNED
2002-04-03 14:44:18 EST	jean-michel_lemieux	Status	RESOLVED	NEW
2002-04-03 14:44:18 EST	jean-michel_lemieux	Resolution	FIXED	---
2002-04-09 09:16:09 EDT	jean-michel_lemieux	Status	VERIFIED	RESOLVED

(b) TossingPath.rar -- This dataset shows the tossing path of a bug report. All developers in the tossing path have participated in the fixing process, and the last developer of the path is the one who finally fixes the bug report. For example, in "8.csv" the bug report ("BugID"=10407) is tossed by 8 times until it is being fixed.  
BugID	 Dev1	 	 	 Dev2 	 	 Dev3 	 	 Dev4 	 	 Dev5 	 	 Dev6 	 	 	 	 Dev7 	 	 	 	 Dev8
10407	kevin_haaland	mike_wilson	grant_gayed	nick_edgar	tod_creasey	kai-uwe_maetzel	platform-text-inbox	daniel_megert
13895	nick_edgar	randy_giffen	tod_creasey	chris_mclaren	csmclaren	debbie_wilson	platform-ui-inbox	bokowski
14856	eduardo_pereira	kevin_haaland	platform-ui-inbox	tod_creasey	mvm	michaelvanmeekeren	platform-swt-inbox	veronika_irvine
15370	dj_houghton	nick_edgar	eduardo_pereira	kai-uwe_maetzel	platform-text-inbox	eclipse	tom_eicher	daniel_megert
15655	erich_gamma	dirk_baeumer	daniel_megert	nick_edgar	randy_giffen	simon_arsenault	chris_mclaren	lynne_kues
16552	klicnik	dejan	nick_edgar	tod_creasey	susan_franklin	susan	platform-ui-triaged	remy.suen
17117	james_moody	nick_edgar	eduardo_pereira	kevin_haaland	platform-ui-inbox	tod_creasey	mvm	michaelvanmeekeren
17528	philippe_mulet	jerome_lanneluc	erich_gamma	adam_kiezun	akiezun	dj_houghton	platform-core-inbox	john_arthorne
18901	nick_edgar	randy_giffen	simon_arsenault	andrew_irvine	eduardo_pereira	airvine	platform-ui-inbox	tod_creasey
```

```
2. DFATPL_Eclipse_input: The input data for the ML classfiers are included in this file. 

(a) feautres_input_TossingProb.csv -- The tossing probability between two developers are listed in this file.

(b) feautres_input.rar -- The feautres inputed for the classfiers in our paper is included in this dataset.
```

## Additional details

The datasets in this paper can be obtained from the raw data in https://github.com/ssea-lab/BugTriage/tree/master/raw%20data/eclipse.
  