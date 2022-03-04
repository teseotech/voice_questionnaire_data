# Voice Questionnaire Data
**The judgments of ADL-based recommendation to evaluate the politeness and persuasiveness of human and synthetic voice.**

> This repository contains the data presented and evaluated in the paper entitled 
> *"Polite Machines Do It Better? A Language-Based Study on Perceived Politeness and Persuasiveness of Virtual Assistants"*,
> which authors are 
> *Marta Cristofanini*, 
> *Luca Buoncompagni*, 
> *Irene Buselli* and 
> *Fulvio Mastrogiovanni*,
> affiliated with 
> [Teseo](https://teseo.tech/),
> [Zenabyte](https://www.zenabyte.com/), and
> the [Department of Informatics, Bioengineering, Robotics and Systems Engineering](https://dibris.unige.it/) of the University of Genoa.
> The paper has been submitted to the 
> [International Journal of Social Robotics](https://www.springer.com/journal/12369) 
> in March 2022.

Please, check the paper for more details about the data and our findings.

## Introduction
We proposed a questionnaire regarding audio-based recommendations for elderly people, which concerned the Activities of Daily Living (ADL), to 40 Italian volunteers.
During the questionaries, volunteers judge the politeness and persuasiveness of sentences spoken by a human (i.e., `Eva`) and synthetic (i.e., `Polly`) voice.
The sentences give recommendations for maintaining a healthy lifestyle, and the questionnaires are available [here](https://forms.gle/RnecqG72HfSCGHfYA) for `Eva`'s voice, and [here](https://forms.gle/bPzJw88PMqJ5siPr7), for `Polly`.

We design recommendations based on different types of communication **strategies**, i.e.,
 - `HP`: Hedged Performatives, 
 - `H`: Hints, 
 - `QP`: Query Preparatory, 
 - `OS`: Obligation Statements.
 
In addition, we design recommendations based on different **intents**, i.e.,
 - `W`: Walking, 
 - `E`: Eating, 
 - `D`: Drinking, 
 - `PH`: Personal Hygiene, 
 - `B` Bathroom visits, 
 - `F` Falls, 
 - `S`: Sleep.

We create 28 recommendations, namely one for each *strategy-intent* combination.
Then we asked the volunteers to rate with a 5-items scale (i.e., `1..5`) the **politeness** of each recommendation, while its **persuasiveness** was rated with a 2-item scale (i.e., `Si` or `No`) representing if the person would follow the recommendation.

## Data Structure
The data collected from the questionnaires is available in a [](CSV file), which columns are organized as follow:
 1. filling **time stamp**, in the format `day/month/year hour:min:sec`,
 2. **age**, i.e., `18-25`, `25-35`, `35-45`, `45-55`, `55-65` or `over 65`,
 3. **gender**, i.e., `Femminile` (female) or `Maschile` (male),
 4. **education level**, i.e., `Licenza elementare o media` (elementary degree), `Diploma di maturità` (high school degree), `Laurea triennale` (Bachelor's degree), `Laurea magistrale o ciclo unico (5 anni)` (master degree), `Dottorato di ricerca` (Ph.D.),
 5. **type of voice**, i.e., `Eva` or `Polly`.

The other columns in the CSV file (i.e., 6-58) contain the volunteers' judgements of the recommendation.
Generally, each recommendation involves two columns, the first shows the politeness rating, while the second addresses persuasiveness.
However, we did not ask to judge the persuasiveness for the recommendations involving the `B` intent.

### Recommendations
It follows the list of recommendations in Italians, and the relative English translation.
The recommendations are organized by intents and strategies.
It is worth noticing that the list below also indicates the number of the CSV column(s) related to each recommendation.

| **Column(s)** | **Intent-Strategy** |                          **Italian Recommendation**                         |                        **English Translation**                       |
|:----------:|:------------:|:---------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
|     6-7    |      W-H     |               Che ne diresti di andare a fare una passeggiata?              |                     How about going for a walk?                     |
|     8-9    |     W-OS     |                         Vai a fare una passeggiata.                         |                            Go for a walk.                           |
|    10-11   |     W-QP     |                        Potresti andare a passeggiare?                       |                       Could you go for a walk?                      |
|    12-13   |     W-HP     |                 Potremmo andare a camminare un po’ se ti va!                |             We could go for a little walk if you’d like!            |
|    14-15   |     E-QP     |                       È ora di pranzo, mangi qualcosa?                      |               It's lunchtime, will you eat something?               |
|    16-17   |     E-HP     |           Si potrebbe mangiare qualcosa se ti va, è ora di pranzo.          |         You could eat something if you like, it's lunchtime.        |
|    18-19   |     E-OS     |                      È ora di pranzo, mangia qualcosa.                      |                    It’s lunchtime, eat something.                   |
|    20-21   |      E-H     |               Che ne dici di mangiare adesso? È ora di pranzo!              |                How about eating now? It's lunchtime!                |
|    22-23   |     D-QP     |                              Ti va dell’acqua?                              |                      Would you like some water?                     |
|    24-25   |     D-OS     |                             Bevi un po’ d’acqua.                            |                          Drink some water.                          |
|    26-27   |      D-H     |                       Che ne dici di bere dell’acqua?                       |                      How about drinking water?                      |
|    28-29   |     D-HP     |         Anche se ti sembra di non avere sete, dovresti bere un po’!         |      Even if you don't feel thirsty, you should drink a little!     |
|    30-31   |     PH-HP    |        Potremmo provare a passare un attimo dal bagno adesso, ti va?        |        We could try to go through the bathroom now, shall we?       |
|    32-33   |     PH-OS    |                          Prova ad andare in bagno.                          |                      Try to go to the bathroom.                     |
|    34-35   |     BH-H     |                  Che ne dici di provare ad andare in bagno?                 |                How about trying to go to the toilet?                |
|    36-37   |     PH-QP    |                  Potresti provare ad andare in bagno, ora?                  |                Could you try to go to the toilet now?               |
|     38     |     B-HP     |     Mi sembra tu stia andando in bagno molte volte oggi, va tutto bene?     | You seem to be going to the bathroom a lot today, is everything OK? |
|     39     |     B-OS     |                    Oggi stai passando molto per il bagno.                   |              You are going to the bathroom a lot today.             |
|     40     |      B-H     |                     Sei spesso in bagno oggi o sbaglio?                     |        You are going to the bathroom a lot today, aren't you?       |
|     41     |     B-QP     |                      Stai andando molto in bagno oggi?                      |              Are you going to the bathroom a lot today?             |
|    42-43   |     F-OS     |                    Mentre avviso i soccorsi parla con me.                   |               While I'm calling for help, talk to me.               |
|    44-45   |     F-HP     |        Ti chiederei, mentre avviso i soccorsi, di provare a parlarmi.       |    I would ask you, while I call for help, to try to talk to me.    |
|    46-47   |     F-QP     |                 Mentre chiamo i soccorsi, parleresti con me?                |             Would you talk to me while I call for help?             |
|    48-49   |      F-H     |              Riesci a parlare con me mentre chiamo i soccorsi?              |              Can you talk to me while I call for help?              |
|    50-51   |      S-H     | Se non prendi sonno, che ne dici di provare a spostarti in un’altra stanza? |  If you don't get sleepy, how about trying to move to another room? |
|    52-53     |     S-QP     |       Ti sposteresti in un’altra stanza per provare a prendere sonno?       |        Would you move to another room to try to get to sleep?       |
|    54-55     |     S-OS     |           Prova a spostarti in un’altra stanza per prendere sonno.          |          Try moving to another room to try to get to sleep.         |
|    56-57     |     S-HP     |       Se per prendere sonno provassimo a spostarci in un’altra stanza?      |  What about trying to move to another room to try to get to sleep?  |

---
