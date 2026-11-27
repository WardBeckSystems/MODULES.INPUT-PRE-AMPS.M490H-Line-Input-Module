# M490H Line Input Module · Input Pre Amps

Ward-Beck Systems M490H, 1978|11. Wiki page: [M490H on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/PAGES/M490H.html)

| Folder | What is in it | Files |
|---|---|---|
| [SCHEMATICS/](SCHEMATICS/) | electrical drawings: schematics, functional diagrams, component layouts, wiring | 29 |
| [MECHANICAL/](MECHANICAL/) | front panels, cover plates, metalwork, assemblies; the front panel as vectors | 24 |
| [PINOUTS/](PINOUTS/) | the RTO-144 connector: connection sheets, connector layouts, rear views | 6 |
| [MANUALS/](MANUALS/) | manuals, manual pages, price lists, brochures, documents | 204 |
| [PHOTOS/](PHOTOS/) | photographs of the module | 1 |
| [SOFTWARE/](SOFTWARE/) | program listings, firmware, the plugin | 1 |
| [KICAD/](KICAD/) | KiCad schematics traced from the drawings, the symbol, PCB projects | 9 |
| [OCR/](OCR/) | the note of every file: date, origin, title block, OCR text | 35 |

<!-- module data: tools/module_specs.py, tools/forum_quotes.py -->

**On the WBSps forum (2006|39 - 2014|47):** [3 topics](FORUM.md): what owners and technicians said about it.

## Specifications

From the technical data sheet: [1978 - M490H - Line Input Module (2).pdf](MANUALS/1978%20-%20M490H%20-%20Line%20Input%20Module%20(2).pdf) page 2 (read by OCR; check against the page). As data: [`Specifications.json`](Specifications.json).

| | |
|---|---|
| **Input Sen slt l v llY** | 10 to +20 dBm (ref. 600 onm source). |
| **Frequency response** | +/-0.5 d B from 30 Hz to 20 kHz. |
| **No l . e** | 70 dBm below nominal ope ratinll level, w1th SENSITIVITY set III -10 dBm, ml.. l nll an enua tor.et at 15 dB &quot; In hand &quot; 120 Hz t o 20 kHz). Noised ec..eases a s S£NSITI VI TY 15 d ec..eased. |
| **Harmonic distortion** | on: Less than 0.3SS THD from 30 Hz 10 20 kHz a l 20 dB above nominal ope..atlng level or less. Less than O. I Sal 1 kHz al 20 d B above |
| **Nom l n e l QI** | lerati n g level or less. Less Ihan 0.51 at 1 kHz throullh cue Channel at 20 dB above nominal |
| &nbsp;&nbsp;QI | leralin$l level or less. |
| **Source impedance** | 600 ohms, b al anced/unbal.nced. |
| **Input impedance** | 24,000 ohms. |
| **Output impedances** | 30,000 on ms, balanced (pl&quot;Og,.am c ircul lS). 60,000 ohms, balanced (cu e circuit.). |
| **Output level** | o dBm nominal, +25 dBm ma.. imum (equ i v alent volta g e 600 ohms). |
| **Phasing** | Input and output t e.....,n.ls designated by numbe&quot;s er-e in phase, or lower n u mbe,. of numbered p a i,. I sIn phase with lower numb _ of other numbered pair: |
| **Logic Inpul Level l'** | (to QI:le,.ale CH ON, CH OFF (; CUE). |
| &nbsp;&nbsp;Logic 0 | 0 10 +13 volts. |
| &nbsp;&nbsp;Logic I | +16 to +24 v e ua, |
| **E.tternal Conlrol OUIPU l** | (Open eeuectee c u..rent sink). |
| **Minimum load impedance** | 600 ohms. M~Il&lt;1 mUm load cu....enl: 40 mAo. |

## Circuit description

From [1978 - M490H - Line Input Module (2).pdf](MANUALS/1978%20-%20M490H%20-%20Line%20Input%20Module%20(2).pdf) pages 5-10 (read by OCR; check against the pages). As data: [`CircuitDescription.json`](CircuitDescription.json).

<details><summary>Read it</summary>

P..os.... m Ch.. nnel Swi lch

2 2 Is II CMOS an lliog switch, se..v l n gas the IIclive s w i l chin gel eme n l of Ih e PROGRAM channel. The cont r-ol voltage t o ocer-e t e Z2 i s de.. lved from Ih e logic cil&quot;'Cuit ry within the module and Is coupled to Z2 viII CR I. to switch the ch &quot;nnel ON, this control voltllge Is I nth e o..d er of &quot;'0 volts. When the control v oll llg e drops to 0 volts, the switch will b e OFF,..es ult ing in II signal a tten u a t ion of more than 100 dB.

FOllowing Z2, Integrated circuits Z3 lind Z4 amplify the lIud io. Ig n ll l to a nominal level of 0 dBm { Ilqui val enl voltage). From the &quot; mpH f le r outpvt, Ih e.I g n a l Is routed 10 the PROGRAM ASSIGN sw i l che. SW4, SWS, SW13, SW14 followed by the mixing bus ou lput s.

Pr Ogrllm Outputs

Fou.. PROGRAM output. PI, P2, P3 6 P4, lire d e.lgned to feed Into four mixing buses. Ope..ation of ASSIGNMENT SWITCHES SW4, SWS, SW13 6 SW14 will r esvlt in I he II U i g n men t of Ih e PROGRAM to the II p prop r l ll le mixing buses.

The CUE.Igna l originate. from abridging lake off a t the Input of the. l l de a tt enuator. Owing to the high Input Imp e dance of Ihe CUE channel lI s ope..ation has no effect On I he main PROGRAM chllnnel. ZS..epr esent s thea u d ios w i l c h for the CUE channel. Simi l&quot;rly to Z 2, the control voltage for 2S I s generated in th&quot; logic c il&quot;'Cuitry li See ee..i bed further on. The output of 2 5 I. followed by the booster amplifier 26, which in lu..n feeds I he eve bus mix ing network R l0l through R104.

The control voltages required to op e..a te Ih e PROGRAM sw i l Ch Z2 and the CUE switch 2S are generated wllh the aid of logic circuitry utilizing Integ..al ed circuits 21 through 210.

l8 i saC MOS dual flip-flop serving as a latch t o maintain the status of l 2 and Z5, once they have been set to either the ON or the OFF position.

A number of Individual Input functions govern the status of the dual flip_flop l8. A description of each Input fun c t ion follows:

When power Is Initially applied to the system, the combination of CR9, CR10, CRll and CR40 will pull down both &quot;dear&quot; inputs of Z8 until C40 Is fully ch ar&quot;g ed, thus ensuring that switch es Z2 and ZS are in the OFF position.

Momentar&quot;Y operation of the CHANNEL ON switch SW9 will produce a negative going pulse at Z8, pin 2 and &quot;prese t &quot; the Ase(; tion of Z8. Alternatively, a momentary ground clo sur&quot;e oft he EXTERNAL CHANNEL ON control input at P2, pin N will result Int h e same condition.

Once the flip_flop Is &quot; pr&quot; ese t &quot;, Its output a t pin I S changes from 0 t o I (app ro xi mate l y +10 volts). This will cause the PROGRAM switch Z2 to switch ON. Furthermore, Ot2 will saturate resulting int h e CHANNEL ON Ind ic a tOr&quot; lamp OS3 to switch on. With QI2 sat u N l ted, the &quot;control common &quot; potential app ears at the emll te r s of 0 13 and 0\4. Apo sitiv e base potential is applied toe i the r&quot; 01 3 or 01 4, depend ing On whether INPUT SELECTORs witch SWI or SW2 I s depressed. Eff e(;t lvely 0 13 and 0 14 operates l m l l a r&quot;l y to l WO AND gates. The coueerce soft he two transistors represent the outputs of the AND gates. They app ear a t P2, pin 13 and P. These terminals are capable of sinking a maximum current of 40 mA each from 1I 24 volt source and mllY be used fOr&quot; muting purposes.

When operating the CHANNEL ON switch SW9, 1I separate contact Is closed, accessible atP 2, pins I S/ S. This contact maybe used for s i multan eo us &quot; machine stll r&quot;t&quot;.

Pin R of P2 i s isolated through diode CR3. When connected in parallel

with the same output of other modules, it provides a convenient OR gale co nfigurlltion, suitable to r&quot;e set a common timer&quot; each time a

CIiAN NEL ON button is depressed.

Mome t ar-y op er-atio... of the CHANNEL OFFs w ilc h SW8 or mom e...tary g rou d cl o sur-e of the EXTERNAL CHANNEL OFF control i...put at 1'2, pi... 12 will r-e sult 1... a...eg a ti v e goi...g pulse a t ZB, pi... 3 a...d -cte e e'' the esee ue... of Z8, pr-oduci...g 0 volts at Z8, pi... 15. cco eeco e...uv, Z2 wills witch OFF, a12 wills top conduC II g, eeusr...g 053 toe x t l...gui sh, a...d the mutl...g contr-ol outputs al 1'2, pis 13 a...d P will be disabled.

A separ-at e cont act 15 available 0... SW8 a...d I s accessible at 1'2, p i...s 17/U. It maybe used for- &quot;maChine stop &quot;.

A sep a r-at e CHANNEL OFF tally lamp Is built I...to 5W8 a...d is connected to P2, 1'1...5 18/V.

The asecuc... of ZB i s used to control the solids tate cue switch 25. The flip-flop will en e...ge state each lime a...eg a t l v e goi...g tr-a n s l t lon takes place a t pi... 6 of 28. Consequently, with each I...pu t pulse, the CUE ch a...n el willa l te r-...ate eetw een ON a...d OFF.

This ee e...g e of slate ce... be brought about by any c...e of three dlffer-e...t methods:

a) Mom e t ar-y op er-ation of the CUEs witch SW12 (a). b } Mome tary grou...d closur-e of the EXTERNAL CUE co...trol I...p ut at P2, pi... II.

cl oceee uc... of the &quot;ov er-pres s&quot; switch SW11, located at at te...u.. torb eyo...d the &quot; I...f l...l l e &quot; posltlon,

The ON status of the CUE cha......e r is i...e ace ree by 052, dr-i v e... by all.

A..... dditione 1 f e.. ture e...sures th.. t the CUE che......e r will.. I ways switch to OFF w he...everth esl ide atte...u atori s moved c...to orawa y

fr-om the &quot;I...fl...l te &quot; po sltio n, r-egar-dl e ss of its pr-iors tate. The cco n-er

5 i g...a l forthi saC llon i s i...lti ated by the cha&quot;'ge of state of theA TTE NUA TOR CUTs witCh 5W10. The ee svn e...t level cne n ge, b el g

ej the rp os it iv e or-...ega t i ve goi...g,; 5 processed through Z 7, Z9 a d

Z 10.

WARO ·SEC K BY STEMS LTO.

The output p..oduced at pin 4 of Z10 wIlla l ways b e a negative going pulse of app r-ox lm atel y 500 mill i seconds du..euen • CRI2 passes this pulse to Z8, pin 8, the r:eb y &quot;c lea.. ing&quot; the B-section of the flip-flop, and r-es u l ting in pin II of Z8 10 switch to (0....ema ina t} 0 volts, i n tu..n switch ing the CUEs witch Z5 to OFF.

All logic control Inputs e r-e buffe r-ec to gu a..d against sp u r-i ou s noise and switch bounce.

Pow e.. Supply Decou p l1ng

Po...e rs u p ply dec oupl lng i s provided b y R146 toR I4 9 and C50 to C53. CR16 and CR 17 se r-v e top..even t ampl lf l e.. damage Int h e event o f supply voltage r eve..s a l. The d ecOlJp l l ng n etwo..k drops the +/ _25 volt supply r-a il s to a nominal voltage of +/_ 18 volts. 01 5 d ecOlJpl es and fllte r-s the positive supply.... ii,.. esu l ting In an output o f +12 volts to ope r:a te the CMOS cb-cu f e.. y. In.. ddit lon, Z3 and Z4 a &quot;e f u.. the r: decoupl ed by R54, R55, C21 and C22.

DESCRIPTION MFG PART NUMBER

Al le r'lUll lOr Ic/w cOl'm ecl or) P.G 1550 / AH35 /100

C, C l!l P ~ c ll or 0.01 of Aee tee CQ92MC103M C2 560 p F Ph !! l p 5 2222-630-03561 CJ 47pF 2222-6JB-70479 C4 4.7 &quot;uF /25 V Kernel TJ9 OC475M025AS

C. 2.2 p F Ph:,l l p 5 2222 _6JB _0322 8 C7 3.9 pF 2222-6JB-09398 C8 150 u F/6 V Ke mel T390 EI57M OO6AS C, 10 uF /25 V T39OC106M025 AS CIO 220 uF/10 V T390 F227MOIOAS

CI1 150 pF Ph, t,ll p 5 2222-638-70151 C12 4.7 pF 2222 -638-09478 cia 220 uF /to V T390F227M010AS cte 4.7 uF /to V T39OB475M010AS COS 4.7 u F/ I O V

ere 0.33 uF /35 V T390A334M 035AS crz 10 uF /2 5 V T390C 106M025AS CI8 10 u F/25 V C&quot; 4.7,f'F P h~,llp 5

C21 47 u F/25 V 426ETF47

O2J 33 ~,F/ I O V T390D336M 0 10AS

C2S 68 00 p F

C26 2.2 u F/ 25 V T39OB225M025 A.S C27 4.7 u F/ l0 V T39OB475M0 10AS

C29 6.8 u F/16 V T39OB68SM0 16AS

CJ&gt; 4.7 &quot;uF /l 0 V T39OB47SMOIOA$

03 2

WA~ CBECK SYSTEMS LTC.

DESCRIPTION MFG PART NUMBER

C33 C ap~c1tor 6800pF Asel eo e092_MC_682M C34 2.2 uF / 25 V Keme t T39QB225M025AS CJ5 0.1 uF /35 V T390 Al04M035 AS

CJ6 delete CJ7 Cap ~eltor 0.1 uF /35 V Kemet n90A104M035 AS CJ8 1 uF/35 V T39OB105M035AS

esc 47 u F/25 V T390E476M0 25AS

COl 1 u F/35 V T3906105 M035 AS m 4.7 uF / l0 V T390B475 M010AS W 2.2 uF /25 V T3906225M025AS CU 1 uF/35 V T39OB105M035 AS css 10 uF /25 V T39OC106M025 AS

C46 6800 pF C092-MC-682M W delete C&lt;8 e ap ~c1tor 10 ~,F/25 V Keme t n9OC106M025AS

CSO 22 uF /2 5 V Philips

CRl Diode Fairchild lN4148

CRJ Motorola lN4003 CR. Fairch ild lN4148

CR' delete

CR' Diode cere

</details>

<!-- /module data -->

## Mechanical

_Mechanical drawings: front panels, cover plates, metalwork and hardware (-03- drawings), AutoCAD files, each with its `(EXTRACTED).svg` vectors; `<module> - front panel.svg` is the front panel as vectors._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKeC1qd1BBNlBqY2s/view?resourcekey=0-M_zR1bsydH61-IGfWxPvJQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKeC1qd1BBNlBqY2s&resourcekey=0-M_zR1bsydH61-IGfWxPvJQ" width="240" alt="1978 - M490H - 490-04-017 - CUE OUT RIGHT OFF TALLY.jpg"></a><br><sub>1978|11 · 490-04-017 - CUE OUT RIGHT OFF TALLY · <a href="MECHANICAL/1978%20-%20M490H%20-%20490-04-017%20-%20CUE%20OUT%20RIGHT%20OFF%20TALLY%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKOWM0SmVDTmo3bm8/view?resourcekey=0-ZjTFPK5w91-Tebtzim2ATw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKOWM0SmVDTmo3bm8&resourcekey=0-ZjTFPK5w91-Tebtzim2ATw" width="240" alt="1978 - M490H - 490-04-017 - LINE INPUT MODULE.jpg"></a><br><sub>1978|11 · 490-04-017 - LINE INPUT MODULE · <a href="MECHANICAL/1978%20-%20M490H%20-%20490-04-017%20-%20LINE%20INPUT%20MODULE%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKSzRiR0tHa1gzLTA/view?resourcekey=0-ZYFCStbA5PMXXQwxOHn9TA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKSzRiR0tHa1gzLTA&resourcekey=0-ZYFCStbA5PMXXQwxOHn9TA" width="240" alt="1978 - M490H - 490-04-018 - MOVING THE SLIDE JTTENUATOR BEYOND THE INFINITE POSITION.jpg"></a><br><sub>1978|11 · 490-04-018 - MOVING THE SLIDE JTTENUATOR BEYOND THE INFINITE POSITION · <a href="MECHANICAL/1978%20-%20M490H%20-%20490-04-018%20-%20MOVING%20THE%20SLIDE%20JTTENUATOR%20BEYOND%20THE%20INFINITE%20POSITION%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKdU5vTjRWZmU1Nm8/view?resourcekey=0-7Us8ZEkIu1nrTNsVIdUqdw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKdU5vTjRWZmU1Nm8&resourcekey=0-7Us8ZEkIu1nrTNsVIdUqdw" width="240" alt="1978 - M490H - 490-04-018 - SWIL WHEN THE SIGNE VIA MIXING NETWORKS.jpg"></a><br><sub>1978|11 · 490-04-018 - SWIL WHEN THE SIGNE VIA MIXING NETWORKS · <a href="MECHANICAL/1978%20-%20M490H%20-%20490-04-018%20-%20SWIL%20WHEN%20THE%20SIGNE%20VIA%20MIXING%20NETWORKS%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1RnSuZhk2OB9jScEHGeUHBlddkebyn8yN/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1RnSuZhk2OB9jScEHGeUHBlddkebyn8yN" width="240" alt="19xx - M490H - DOC - 90-04-017 - PROGRAA CHUNNE THE BUILT-IN DAY LAMP.jpg"></a><br><sub>19xx - M490H - DOC - 90-04-017 - PROGRAA CHUNNE THE BUILT-IN DAY LAMP · <a href="MECHANICAL/19xx%20-%20M490H%20-%20DOC%20-%2090-04-017%20-%20PROGRAA%20CHUNNE%20THE%20BUILT-IN%20DAY%20LAMP%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## Schematics

_Electrical drawings: schematics (-02-), functional diagrams (-01-), component layouts (-06-), wiring (-09-), PCB files (.pcb .dsn), and beside each scan its `(EXTRACTED).svg`: the vectors traced from it._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKN3ZBRmdnd1FydVk/view?resourcekey=0-73T_kHgQVnroE-fCG4HeFQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKN3ZBRmdnd1FydVk&resourcekey=0-73T_kHgQVnroE-fCG4HeFQ" width="240" alt="1978 - M490H - 490-01-009 - LINE INPUT MODULE FUNCTIONAL DIAGRAM.jpg"></a><br><sub>1978|11 · 490-01-009 - LINE INPUT MODULE FUNCTIONAL DIAGRAM · <a href="SCHEMATICS/1978%20-%20M490H%20-%20490-01-009%20-%20LINE%20INPUT%20MODULE%20FUNCTIONAL%20DIAGRAM%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKT3MtNWlITGFMTHM/view?resourcekey=0-kS_O9W1CaLstTNCmEy7fXA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKT3MtNWlITGFMTHM&resourcekey=0-kS_O9W1CaLstTNCmEy7fXA" width="240" alt="1978 - M490H - 490-01-009 - TIMER RESET OFF TALLY OFF.jpg"></a><br><sub>1978|11 · 490-01-009 - TIMER RESET OFF TALLY OFF · <a href="SCHEMATICS/1978%20-%20M490H%20-%20490-01-009%20-%20TIMER%20RESET%20OFF%20TALLY%20OFF%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKUFB4c2RYS3hnMVk/view?resourcekey=0-X8PnY2FlBD-76xRxYokO0g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKUFB4c2RYS3hnMVk&resourcekey=0-X8PnY2FlBD-76xRxYokO0g" width="240" alt="1978 - M490H - 490-02-009 - CAST COMPONENT DESIGNATIONS CRIC.jpg"></a><br><sub>1978|11 · 490-02-009 - CAST COMPONENT DESIGNATIONS CRIC · <a href="SCHEMATICS/1978%20-%20M490H%20-%20490-02-009%20-%20CAST%20COMPONENT%20DESIGNATIONS%20CRIC%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKX25Vb2ZPU2RabTQ/view?resourcekey=0-kUNm9Cs_-agB3EOFp1HX4g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKX25Vb2ZPU2RabTQ&resourcekey=0-kUNm9Cs_-agB3EOFp1HX4g" width="240" alt="1978 - M490H - 490-02-009 - LINE INPUT MODULE.jpg"></a><br><sub>1978|11 · 490-02-009 - LINE INPUT MODULE · <a href="SCHEMATICS/1978%20-%20M490H%20-%20490-02-009%20-%20LINE%20INPUT%20MODULE%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZHRNRUMyR1BWMkU/view?resourcekey=0-LNRA9QiFz3Gz1BcrqSkZvQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZHRNRUMyR1BWMkU&resourcekey=0-LNRA9QiFz3Gz1BcrqSkZvQ" width="240" alt="1978 - M490H - 490-06-019 - ISSU IDATE REVISION.jpg"></a><br><sub>1978|11 · 490-06-019 - ISSU IDATE REVISION · <a href="SCHEMATICS/1978%20-%20M490H%20-%20490-06-019%20-%20ISSU%20IDATE%20REVISION%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKVmd4N0UxdWEyWkU/view?resourcekey=0-_pd2DYe2DR6JKyUt9hES-w" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKVmd4N0UxdWEyWkU&resourcekey=0-_pd2DYe2DR6JKyUt9hES-w" width="240" alt="1978 - M490H - 490-06-019 - LINE INPUT MODULE.jpg"></a><br><sub>1978|11 · 490-06-019 - LINE INPUT MODULE · <a href="SCHEMATICS/1978%20-%20M490H%20-%20490-06-019%20-%20LINE%20INPUT%20MODULE%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

Shared privately on Google Drive (opens after sign-in): [1978|11 · 490-06-019](https://drive.google.com/file/d/0B0yR0b5T78SKSmhlTGVodjdUMEU/view?resourcekey=0-Y6R7EQErPugQdTr3P3kG2g)

## Pinouts

_Pinouts: the RTO-144 edge connector (connection sheets, connector layouts and rear views, strapping), and the pinout / connections drawings made from them. The module root `RTO.json` lists every contact._

Not on Google Drive yet: `M490H - RTO-144 Connections.pdf`

## RTO-144 pinout

22 contacts, 4 contacts (P1), 21 contacts (P2). Every contact, with where it was read: [`RTO.json`](RTO.json).

| Pin | Signal | Kind | Pair | Confidence |
|---|---|---|---|---|
| 1 | LEFT PGRM 1 | audio | A3 + | high |
| 1 | MIC IN A | in | A1 + | high |
| 2 | PGM | audio |  | high |
| 2 | LEFT PGRM 1 | audio | A3 - | high |
| 3 | PGM 3 OUT | out |  | high |
| 3 | RIGHT PGRM 1 | audio | A4 + | high |
| 3 | MIC IN B | in | A2 + | high |
| 4 | PGM 3 OUT | out |  | high |
| 4 | RIGHT PGRM 1 | audio | A4 - | high |
| 5 | PGM 2 OUT | out |  | high |
| 5 |  | unread |  | low |
| 6 | PGM 2 OUT | out |  | high |
| 6 | INSERT SEND | out | B1 + | high |
| 7 | PGM 4 OUT | out |  | high |
| 7 | INSERT RETURN | in | B2 + | high |
| 8 | PGM 4 OUT | out |  | high |
| 8 |  | unread |  | low |
| 9 | SHIELD | ground |  | high |
| 10 | NC | nc |  | high |
| 11 | IC | nc |  | high |
| 12 | IC | nc |  | high |
| 12 |  | unread |  | low |
| 13 | IC | nc |  | high |
| 14 | IC | nc |  | high |
| 15 | CUE OUT, LEFT | out |  | high |
| 15 |  | unread |  | low |
| 16 | CUE OUT, LEFT | out |  | high |
| 17 | CUE OUT, RIGHT | out |  | high |
| 17 |  | unread |  | low |
| 18 | CUE OUT, RIGHT | out |  | high |
| 18 |  | unread |  | low |
| 19 | NC | nc |  | high |
| 19 | -25 V | power |  | high |
| 20 | NC | nc |  | high |
| 20 | COMMON | ground |  | high |
| 21 | NC | nc |  | high |
| 21 | +25 V | power |  | high |
| 22 | CHASSIS | ground |  | high |
| A | MIC IN A | in | A1 - | high |
| C | MIC IN B | in | A2 - | high |
| E |  | unread |  | low |
| F | INSERT SEND | out | B1 - | high |
| H | INSERT RETURN | in | B2 - | high |
| J |  | unread |  | low |
| L |  | unread |  | low |
| M |  | unread |  | low |
| N |  | unread |  | low |
| P |  | unread |  | low |
| U |  | unread |  | low |
| V |  | unread |  | low |

**Straps:** Insert: JMP.6.7 · Insert: JMP.F.H

## Manuals and documents

_Manuals and manual pages, price lists, RTO-144 connection sheets, brochures, ads and other document scans._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKX20tVUZKY1c3TzQ/view?resourcekey=0-41CqOh3GHAjmZZrQivxkqg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKX20tVUZKY1c3TzQ&resourcekey=0-41CqOh3GHAjmZZrQivxkqg" width="240" alt="1978 - M490H - Line Input Module (2).pdf"></a><br><sub>1978|11 · Line Input Module (2)</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKWjc3c05ESFR4TG8/view?resourcekey=0-eME8OzM_9Z--TGRiktW-tw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKWjc3c05ESFR4TG8&resourcekey=0-eME8OzM_9Z--TGRiktW-tw" width="240" alt="1978 - M490H - Line Input Module.pdf"></a><br><sub>1978|11 · Line Input Module</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKb1VwdlNDbllTck0/view?resourcekey=0-4PvTvfUhslJPaQZ4hzC5XA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKb1VwdlNDbllTck0&resourcekey=0-4PvTvfUhslJPaQZ4hzC5XA" width="240" alt="1978 - M490H - P001 - Title Page.jpg"></a><br><sub>1978|11 · P001 - Title Page</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKMmdQMndiZnlpRTg/view?resourcekey=0-Ri5QB0X-7-wroTIHzkFONA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKMmdQMndiZnlpRTg&resourcekey=0-Ri5QB0X-7-wroTIHzkFONA" width="240" alt="1978 - M490H - P002 - 1-1.jpg"></a><br><sub>1978|11 · P002 - 1-1</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNkJUUTh6VF90eVU/view?resourcekey=0-ubD7zN9PSMWWS4fX_Y6NwQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNkJUUTh6VF90eVU&resourcekey=0-ubD7zN9PSMWWS4fX_Y6NwQ" width="240" alt="1978 - M490H - P003 - 1-2.jpg"></a><br><sub>1978|11 · P003 - 1-2</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKS2ZjZlhNUHB3UWc/view?resourcekey=0-Yj7xF5PFfRGtyEnsTrK10Q" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKS2ZjZlhNUHB3UWc&resourcekey=0-Yj7xF5PFfRGtyEnsTrK10Q" width="240" alt="1978 - M490H - P004 - 2-1.jpg"></a><br><sub>1978|11 · P004 - 2-1</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKY2tCS3Z4Y05oM2s/view?resourcekey=0-f3209ywUkN0YpMCwZRtcKw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKY2tCS3Z4Y05oM2s&resourcekey=0-f3209ywUkN0YpMCwZRtcKw" width="240" alt="1978 - M490H - P005 - 2-2.jpg"></a><br><sub>1978|11 · P005 - 2-2</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbHhpRUt2TnZnbzQ/view?resourcekey=0-AeeqfiTWpagVGf3CPcuwtw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbHhpRUt2TnZnbzQ&resourcekey=0-AeeqfiTWpagVGf3CPcuwtw" width="240" alt="1978 - M490H - P006 - 2-3.jpg"></a><br><sub>1978|11 · P006 - 2-3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKelZLUVVPN2dHbzg/view?resourcekey=0-OOvlKv7V0aGJNL_wxbnrUQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKelZLUVVPN2dHbzg&resourcekey=0-OOvlKv7V0aGJNL_wxbnrUQ" width="240" alt="1978 - M490H - P007 - 2-4.jpg"></a><br><sub>1978|11 · P007 - 2-4</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKdG56NERXVXYyQmc/view?resourcekey=0-GVq5H-UshCO0L8TWrhH7dA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKdG56NERXVXYyQmc&resourcekey=0-GVq5H-UshCO0L8TWrhH7dA" width="240" alt="1978 - M490H - P008 - 2-5.jpg"></a><br><sub>1978|11 · P008 - 2-5</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZ1IweXRvZUVkc3M/view?resourcekey=0-WINzzBcIoScroBrVsaiSeA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZ1IweXRvZUVkc3M&resourcekey=0-WINzzBcIoScroBrVsaiSeA" width="240" alt="1978 - M490H - P009 - 3-1.jpg"></a><br><sub>1978|11 · P009 - 3-1</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKOFRTTzRENDl4aDg/view?resourcekey=0-ymta9YzP8kMpqYlweqpN3Q" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKOFRTTzRENDl4aDg&resourcekey=0-ymta9YzP8kMpqYlweqpN3Q" width="240" alt="1978 - M490H - P010 - 3-2.jpg"></a><br><sub>1978|11 · P010 - 3-2</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKS3FGQVNmQlZlcVE/view?resourcekey=0-dGMQnLWpPKTP2J8af6VJmg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKS3FGQVNmQlZlcVE&resourcekey=0-dGMQnLWpPKTP2J8af6VJmg" width="240" alt="1978 - M490H - P011 - 3-3.jpg"></a><br><sub>1978|11 · P011 - 3-3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKSGlxS2J1N2lmR2s/view?resourcekey=0-KVG9ArBs9GawsSxAZ7FvJA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKSGlxS2J1N2lmR2s&resourcekey=0-KVG9ArBs9GawsSxAZ7FvJA" width="240" alt="1978 - M490H - P012 - 3-4.jpg"></a><br><sub>1978|11 · P012 - 3-4</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKUGhNalNmNzJjQTg/view?resourcekey=0-ov_3-LIkRotOShHDFtDzug" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKUGhNalNmNzJjQTg&resourcekey=0-ov_3-LIkRotOShHDFtDzug" width="240" alt="1978 - M490H - P013 - 3-5.jpg"></a><br><sub>1978|11 · P013 - 3-5</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKWk1UQWx0Wnpac2M/view?resourcekey=0-nK6wtt0xLMoT1HnCGf0e9Q" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKWk1UQWx0Wnpac2M&resourcekey=0-nK6wtt0xLMoT1HnCGf0e9Q" width="240" alt="1978 - M490H - P014 - 3-6.jpg"></a><br><sub>1978|11 · P014 - 3-6</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKckdGN0o2SmNNdlU/view?resourcekey=0-rIufjQ5RFSAITEec1CiqKA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKckdGN0o2SmNNdlU&resourcekey=0-rIufjQ5RFSAITEec1CiqKA" width="240" alt="1978 - M490H - P015 - 3-7.jpg"></a><br><sub>1978|11 · P015 - 3-7</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcWJoSWFXUG9IenM/view?resourcekey=0-76MKcCQh-vZqJgq2SdI8oA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcWJoSWFXUG9IenM&resourcekey=0-76MKcCQh-vZqJgq2SdI8oA" width="240" alt="1978 - M490H - P016 - 3-8.jpg"></a><br><sub>1978|11 · P016 - 3-8</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKUVZJWVF2TXpDMWs/view?resourcekey=0-27tsy3zrIqNtKIJb1jqYPA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKUVZJWVF2TXpDMWs&resourcekey=0-27tsy3zrIqNtKIJb1jqYPA" width="240" alt="1978 - M490H - P017 - 3-9.jpg"></a><br><sub>1978|11 · P017 - 3-9</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKa1pNNmxXNk1QWTQ/view?resourcekey=0-BLCaQK3LI2e61J69Kh7EOw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKa1pNNmxXNk1QWTQ&resourcekey=0-BLCaQK3LI2e61J69Kh7EOw" width="240" alt="1978 - M490H - P018 - CD4016.jpg"></a><br><sub>1978|11 · P018 - CD4016</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKdlNocV9hYjNpWkE/view?resourcekey=0-B87sDEROr-dmgczgOlgKpA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKdlNocV9hYjNpWkE&resourcekey=0-B87sDEROr-dmgczgOlgKpA" width="240" alt="1978 - M490H - P019 - 74C76.jpg"></a><br><sub>1978|11 · P019 - 74C76</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNlZMTW1CU3RPZjQ/view?resourcekey=0-VExwwDbaPv3F_PmmYcNMRA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNlZMTW1CU3RPZjQ&resourcekey=0-VExwwDbaPv3F_PmmYcNMRA" width="240" alt="1978 - M490H - P020 - 74C221.jpg"></a><br><sub>1978|11 · P020 - 74C221</sub></td></tr>
</table>

Not on Google Drive yet: `20130725 - WBS M490H MODS.jpg`

## KiCad

_KiCad: a schematic (`.kicad_sch`) traced from each electrical drawing, the module symbol (`.kicad_sym`) and its PCB projects. Traced schematics are the line work only: redraw with symbols over them._

- [1978 - M490H - 490-01-009 - LINE INPUT MODULE FUNCTIONAL DIAGRAM.kicad_sch](KICAD/1978%20-%20M490H%20-%20490-01-009%20-%20LINE%20INPUT%20MODULE%20FUNCTIONAL%20DIAGRAM.kicad_sch)
- [1978 - M490H - 490-01-009 - TIMER RESET OFF TALLY OFF.kicad_sch](KICAD/1978%20-%20M490H%20-%20490-01-009%20-%20TIMER%20RESET%20OFF%20TALLY%20OFF.kicad_sch)
- [1978 - M490H - 490-02-009 - CAST COMPONENT DESIGNATIONS CRIC.kicad_sch](KICAD/1978%20-%20M490H%20-%20490-02-009%20-%20CAST%20COMPONENT%20DESIGNATIONS%20CRIC.kicad_sch)
- [1978 - M490H - 490-02-009 - LINE INPUT MODULE.kicad_sch](KICAD/1978%20-%20M490H%20-%20490-02-009%20-%20LINE%20INPUT%20MODULE.kicad_sch)
- [1978 - M490H - Line Input Module (2) p24.kicad_sch](KICAD/1978%20-%20M490H%20-%20Line%20Input%20Module%20(2)%20p24.kicad_sch)
- [1978 - M490H - Line Input Module p24.kicad_sch](KICAD/1978%20-%20M490H%20-%20Line%20Input%20Module%20p24.kicad_sch)
- [1978 - M490H - Line Input Module p26.kicad_sch](KICAD/1978%20-%20M490H%20-%20Line%20Input%20Module%20p26.kicad_sch)
- [M490H.kicad_sym](KICAD/M490H.kicad_sym)
- [index.html](KICAD/index.html)

## Software

- [index.html](SOFTWARE/index.html)

---
Archive: Anthony Peter Kuzub · [WBSps.ca](https://WBSps.ca) · [WBSps.Kuzub.com](https://WBSps.Kuzub.com)
