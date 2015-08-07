# Baltimore Riot Emails, as read by LDA

This repository contains scripts to support the creation of topic
models using LDA (Latent Dirichlet Allocation) for the Baltimore Riot Emails
that were recently released. These emails contain correspondence subject to the
Freedom of Information Act between city employees and citizens.

## Topic Modeling

Topic modeling is the idea that documents are mixtures of topics and topics
themselves are mixtures of words. For example, we would expect a collection
of documents about pets to have a topic containing words about cats in addition
to topics containing words about dogs. Topic modeling is a useful way to gain
insight into the themes present in an otherwise unknown collection of documents.

More information on topic modeling is available online.

## Why do I care?

In short, topic modeling can take a large collection of documents, and tell you something
about the themes in those documents. To use an example from the Baltimore Riot Emails topic
model below, it's interesting to note that topic 23 seems to be about the Red Line. This tells
us that city officials were discussing the Red Line during the riots. We didn't have to read
the emails themselves to find that out. There are also a few topics about the curfew, which
might mean that this was discussed throughout the emails in several different contexts. 

## Tooling

The LDA implementation is provided by the open source natural language processing tool
[MALLET](http://mallet.cs.umass.edu/index.php).

The rest is just wired together with shell scripts! All commands were run on Linux, but
they should work fine on Mac provided pdftotext is installed.

## An Example

Below is a sample of 50 topics from the Baltimore Riot Emails dataset. It is important
to reiterate that this is a *sample*. In other words, it is a single result from a statistical
sampling model and should not be construed as "the answer". Said yet another way, n = 1. It is
provided only to give a flavor of the topics in this dataset.

There are 50 topics in all (this is configurable), and each topic is labeled with a number.

```
0	0.00981	subject maryland copy brian maloney bovaird robert khalil sharonlyn kaczynski zaied information cc moit protests mta office attachment message 
1	0.00936	kevin harris mayor mayorsrb stephanie image blake png rawlings hall subject april michael figliola mailto street rawlingsblake office news 
2	0.00433	esf lead emergency department management office mayor official street health public fire regular support police information operating unclassified bpd 
3	0.00722	news police play thumbnail click abc fox nbc cbs today morning gray tx ny freddie people pa arrested fl 
4	0.00629	petition org change people supporters anthony batts md decision apr justice rawlings stephanie blake view police respond makers starter 
5	0.00351	kevin cleary message shannon office april subject protest cosgrove information error mayor info emergency avenue crs attachment fair daniel 
6	0.0153	mail intended org information message curfew recipient subject email attachments confidential sender international received legal immediately amnesty error delete 
7	0.00108	woods lerch southworth dunkes burley baton sine oil hwy blvd shell farms exxon czorapinski park petroleum county eleven agent 
8	0.01194	maryland county sun center hogan school state year balt business million read schools budget funding education larry post monday 
9	0.00767	news baltimoresun html story maryland bs cnn freddie md william subject april zerofox foster veronica gray mcbeth ci thursday 
10	0.00441	maryland mema emergency state pbc center alert april executive region operations subject significant eoc enforcement level management agency county 
11	0.01295	gray police housing freddie protests death officers saturday april black justice van sun commissioner director hall maryland arrest protest 
12	0.00662	department police reform rawlings blake mayor board review civilian stephanie broken md worse gray important needed cases paper recommendations 
13	0.00775	click thumbnail play radio news fm washington ny custody people cable md fox week york boston today men fl 
14	0.00085	archive share words matched translate news police riots mayor curfew fox post obama sources gray cnn abc freddie source 
15	0.0103	health services street department insurance pharmacies call eric north costello residents operations bchd pharmacy mental information prescription expected curfew 
16	0.00587	police bizjournals email business news rights april media freddie purge international edition protests force contact people today read subscription 
17	0.00485	yahoo net hotmail aol gmail org comcast accenture community sbcglobal msn sr kim verizon mi association md marvin dr 
18	0.00944	police news play click thumbnail department ca cable fox officers abc nbc cnn alert san freddie today death arrested 
19	0.01658	andrew smullian subject mikulski april mary cc tuesday message office kevin state pat drew budget vetter curfew update date 
20	0.01524	google police flag irrelevant news alert alerts batts york april coverage unsubscribe received gray subject feed update full subscribed 
21	0.04428	police people april subject community time good don batts mayor make things message violence anthony officers work today department 
22	0.00169	av ro ad le dr er la ra ne road oa larceny auto ll burglary ha il discharging pa 
23	0.00552	line transit red maryland purple economic jobs transportation ai cost lines rail state benefits light observers region future pdf 
24	0.03196	curfew batts people time neighborhoods commissioner blake rawlings anthony mayor point government residents safety neighbors friends families sidewalks freedom 
25	0.00253	calls total emergency received answered call center time aa ae ac ab af ad services avg riot seconds abandoned 
26	0.03608	howard libit mayor office subject attachment april error kaliope mayorsrb parthemos stephanie blake rawlings connect street md rawlingsblake mobile 
27	0.00233	mayors tom de org usmayors statement andrew apr laura wrote tcochran mayor cochran la today dc ben mariah conference 
28	0.04652	mayor rawlings blake stephanie monday curfew governor state press week day riots rioters hogan thugs leaders justice place national 
29	0.00404	twitter https police media instagram status pay andrew org officers threat youtube meeting trang browndowntown whites april watch hazard 
30	0.02005	police officers man officer people week year lynch case shot arrested department court men involved general mosby gray attorney 
31	0.01468	md subject april anthony martin police cc district william batts ganesha org charles hyatt chief melissa wd baltimorepolice protest 
32	0.02735	community support center school students residents communities public work staff meeting action week events april office org street food 
33	0.00826	nbcuniversal kevin harris subject msnbc april carmen cc morning howard widman jesse rodriguez libit nbcuni request interview alex mayor 
34	0.01523	colin mayor tarbert curfew office business attachment stephanie rawlings error blake mayorsrb april work subject street time hours businesses 
35	0.00504	dawn md health mailto kirstaetter maryland dr molly tierney shannon bcps wen leana angela jacquelyn batts hyatt harvey duval 
36	0.01556	police gray investigation freddie death state attorney department report turned office results findings prosecutors van morning friday day commissioner 
37	0.00706	business businesses bdc mayor maryland assistance development employment contact support office mima economic department information moed owners recovery continue 
38	0.01637	mayor rawlings blake kevin harris statement sean cheryl naron curfew stewart email stephanie subject contact sunday libit howard wide 
39	0.01878	curfew morning night national guard people arrests officers work commissioner overnight sunday back good lifted anthony monday batts effect 
40	0.02828	curfew batts people time neighborhoods commissioner rawlings blake anthony mayor restrictions point streets safety serve friends policy dear demand 
41	0.01792	black american people law government justice state org show white world public president country young african nation policy national 
42	0.0059	maryland org event information contact free md tickets day program saturday street online law live norwich annual center committee 
43	0.00956	subject april org event events cc contact smullian md information steve office apr request tomorrow andrew message street date 
44	0.00652	emergency esf lead management county office mayor department official eoc operations health hrs information fire police incident closed support 
45	0.01083	police national guard riots officers violence state span fire family font law emergency commissioner night monday style looting riot 
46	0.01121	officers gray death police charges freddie charged attorney union criminal state murder face connection prosecutor arrest degree facing involved 
47	0.01101	robert maloney subject scott april connor david mcmillan cc updates saturday minutes uneventful thursday jhu call message district dawn 
48	0.00597	church dr rev bishop baptist call ame pastor peace april augustus gussener list sunday subject clergy sr christ howard 
49	0.00915	job colin tarbert org monday mall mondawmin services center maryland mayor subject employment moed laurie friday email office development 
```
