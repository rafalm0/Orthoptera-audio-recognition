#############################################

Description:

Two newly compiled datasets for training neural networks to automatically identify insect species while comparing adaptive, waveform-based frontends to conventional mel-spectrogram frontends for audio feature extraction. This work was submitted for publication in a journal and the machine learning implementations will be published on Github. 

These datasets expand on the previously published InsectSet32 by including recently published collections of insect recordings by citizen scientists from around the world. Recordings from [BioAcoustica](https://bio.acousti.ca/), [xeno-canto](http://xeno-canto.org) and [iNaturalist](http://iNaturalist.org), as well as private collections by [Baudewijn Odé](https://orcid.org/0000-0002-8929-2737) were downloaded and manually inspected. Files with strong noise interference or intense filtering, as well as files containing sounds of multiple species were removed to compile these datasets. The files were standardised to 44.1 kHz mono WAV files ranging in length from less than one second to several minutes. Files containing long periods without insect sounds were edited into multiple smaller files with silent periods no longer than 5 seconds. These files are marked as edits in the annotation file and should be assigned together into train/validation/test sets to prevent data leakage. The annotation files contain information for each recording, including the file name, species name and identifier, as well as the data subset they were included in for training the neural network (training, test, validation). 

InsectSet47 expands on InsectSet32 with recordings from [xeno-canto](http://xeno-canto.org) and contains 1006 original recordings from 47 species, with at least ten files per species. The total length of InsectSet47 is 22 hours. InsectSet66 further expands on InsectSet47 by adding research-grade audio observations from [iNaturalist](http://iNaturalist.org), with a total of 1554 recordings from 66 species, a total length of over 24 hours and a minimum of ten files per species. The datasets were split into the training, validation and test sets while ensuring a roughly equal distribution of audio files and audio material for every species in all three subsets. This resulted in a 60/20/20 split (train/validation/test) by file number and a 64/19.5/16.5 split by file length.

#############################################

CSV:

The annotation files for both parts of the dataset include information for all recordings:

file_name:	The file name used in this dataset, with the species name attached
species:	The name of the species in the recording (see species list below)
subset:		The data-subset the file was included in for training, testing or validating a neural network
unique_file:	The unique file name for files that were edited into smaller chunks (indicated by “_edit#” at the end of the file name)
link:		The link to the observation on xeno-canto or iNaturalist
contributor:	The contributor/original recordist of the recording

#############################################

InsectSet47:

Species					n	min:s

Chorthippus biguttulus 			52	29:49
Stenobothrus stigmaticus 		39	5:31
Chorthippus mollis 			38	27:35
Gryllus campestris 			38	94:21
Conocephalus fuscus 			34	53:06
Roeseliana roeselii 			33	33:39
Pseudochorthippus parallelus 		33	24:36
Chorthippus brunneus 			32	20:58
Tettigonia cantans 			32	57:15
Decticus verrucivorus 			31	71:30
Ephippiger diurnus 			29	39:33
Gomphocerippus rufus 			28	29:38
Nemobius sylvestris 			28	38:11
Gampsocleis glabra 			26	55:01
Omocestus viridulus 			25	45:25
Tettigonia viridissima 			24	25:30
Acheta domesticus 			23	55:38
Oecanthus pellucens 			22	28:38
Platypleura cf catenata 		22	17:46
Omocestus rufipes 			21	16:28
Pholidoptera griseoaptera 		21	11:46
Chorthippus apricarius 			20	28:27
Phaneroptera falcata 			20	28:29
Myrmeleotettix maculatus 		20	55:06
Platypleura plumosa 			19	14:41
Stenobothrus lineatus 			18	32:41
Conocephalus dorsalis 			18	23:07
Chrysochraon dispar 			17	15:35
Gryllus bimaculatus 			17	27:32
Platypleura sp10 			17	17:55
Phaneroptera nana 			16	29:53
Platycleis albopunctata 		15	24:44
Gomphocerus sibiricus			14	26:04
Barbitistes yersini			14	19:59
Pholidoptera aptera			13	10:31
Pholidoptera littoralis			13	4:00
Metrioptera brachyptera			13	20:29
Leptophyes punctatissima		13	26:47
Pseudochorthippus montanus		12	11:29
Platypleura sp13			12	7:01
Chorthippus albomarginatus		11	40:29
Eupholidoptera schmidti			11	9:39
Melanogryllus desertus			11	25:24
Tylopsis lilifolia			11	3:30
Omocestus petraeus			10	9:21
Chorthippus vagans			10	11:43
Platypleura sp12 cf hirtipennis		10	7:41

#############################################

InsectSet66:

Species					n	h:min:s

Yoyetta celis 				152	0:11:16
Gryllus campestris 			57	1:37:39
Chorthippus biguttulus 			53 	0:30:25
Galanga labeculata 			43 	0:06:16
Yoyetta repetens 			40 	0:05:23
Chorthippus mollis 			39 	0:27:50
Stenobothrus stigmaticus		39 	0:05:31
Pseudochorthippus parallelus		37 	0:25:08
Roeseliana roeselii 			37 	0:34:34
Tettigonia cantans 			37 	0:58:10
Conocephalus fuscus 			36 	0:53:34
Chorthippus brunneus 			35 	0:21:57
Decticus verrucivorus 			34 	1:15:04
Tettigonia viridissima 			33 	0:27:26
Ephippiger diurnus 			31 	0:39:51
Nemobius sylvestris 			30 	0:38:44
Oecanthus pellucens 			29 	0:30:32
Gomphocerippus rufus 			28 	0:29:38
Pholidoptera griseoaptera		27 	0:14:07
Omocestus viridulus 			27 	0:45:48
Gampsocleis glabra 			27 	0:55:18
Acheta domesticus 			24 	0:56:48
Aleeta curvicosta			23	0:04:04
Platypleura cfcatenata			22	0:17:47
Omocestus rufipes			22	0:16:34
Chorthippus apricarius			21	0:28:35
Myrmeleotettix maculatus		21	1:05:37
Cicada orni				21	0:06:50
Phaneroptera falcata			20	0:28:30
Gryllus bimaculatus			20	0:28:44
Platypleura plumosa			19	0:14:42
Stenobothrus lineatus			19	0:34:27
Clinopsalta autumna			19	0:04:16
Phaneroptera nana			18	0:30:50
Conocephalus dorsalis			18	0:23:07
Platypleura sp10			17	0:17:55
Chrysochraon dispar			17	0:15:36
Pholidoptera aptera			16	0:10:55
Eumodicogryllus bordigalensis		16	0:10:56
Platycleis albopunctata			15	0:24:45
Atrapsalta corticina			15	0:02:15
Neotibicen pruinosus			15	0:04:41
Atrapsalta encaustica			15	0:04:33
Metrioptera brachyptera			14	0:20:56
Gomphocerus sibiricus 			14	0:26:05
Barbitistes yersini 			14	0:19:59
Psaltoda plaga 				14	0:04:21
Popplepsalta notialis 			14	0:02:58
Pholidoptera littoralis 		13	0:04:00
Pseudochorthippus montanus 		13	0:11:36
Leptophyes punctatissima 		13	0:26:48
Cyclochila australasiae 		13	0:01:53
Platypleura sp13 			12	0:07:01
Chorthippus albomarginatus 		11	0:40:29
Eupholidoptera schmidti 		11	0:09:40
Melanogryllus desertus 			11	0:25:24
Tylopsis lilifolia 			11	0:03:30
Ruspolia nitidula 			11	0:12:35
Diceroprocta eugraphica 		11	0:05:07
Platypleura sp12cfhirtipennis 		10	0:07:42
Omocestus petraeus 			10	0:09:22
Stauroderus scalaris 			10	0:20:43
Chorthippus vagans 			10	0:11:43
Bicolorana bicolor 			10	0:09:19
Popplepsalta aeroides 			10	0:01:46
Atrapsalta collina 			10	0:01:20

#############################################

Copyright (c) is held by the individual recordists.

These data are published under the Creative Commons Attribution licence (CC BY-SA 4.0):
[https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/)
This licence allows to to re-use the data for almost any purpose (follow the link for more information), as long as you give credit and use the same license as the original source.

For academic reuse, we ask that you do this as a citation to the research paper, given above.