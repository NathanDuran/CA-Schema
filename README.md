# Conversation Analysis Modelling Schema
A Conversation Analysis Annotation Schema for Computational Modelling of Dialogue. 
[Available here](https://nathanduran.github.io/Conversation-Analysis-Modelling-Schema/)

A full explanation of the intended use for the CAMS can be found in the paper 
[Conversation Analysis Structured Dialogue for Multi-Domain Dialogue Management](https://www.researchgate.net/publication/329809503_Conversation_Analysis_Structured_Dialogue_for_Multi-Domain_Dialogue_Management).
If you use this schema please cite:
Duran, N. and Battle, S. (2018) Conversation Analysis Structured Dialogue for Multi-Domain Dialogue Management.
In: The International Workshop on Dialogue, Explanation and Argumentation in Human-Agent Interaction (DEXAHAI) 

A corpus of CAMS labelled dialogue [CAMS-KVRET can be found here.](https://github.com/NathanDuran/CA-KVRET) 

[Overview](#overview-link)
------------

##### &emsp;[Adjacency Pairs (AP)](#ap-overview-link)

##### &emsp;[Dialogue Acts (DA)](#da-overview-link)

##### &emsp;[Adjacency Pair Types (AP-types)](#ap-types-overview-link)


[Annotation Guidelines](#annotation-guidelines-link)
------------

##### &emsp;[Adjacency Pair Sequences](#ap-annotation-guidelines-link)

&emsp; [Base Sequences](#base-sequences)

&emsp; [Pre and Post Sequences](#pre-and-post-sequences)

&emsp; [Insert Sequences](#insert-sequences)

&emsp; [Minimal Expansion](#minimal-expansion)

##### &emsp;[Dialogue Acts and Adjacency Pair Types (AP-types)](#da-ap-types-annotation-guidelines-link)


[Label Definitions](#label-definitions-link)
------------

### [Adjacency Pairs](#ap-label-definitions-link)

##### &emsp;[Base](#base-label-definitions-link)

##### &emsp;[Expansions](#expansions-label-definitions-link)

&emsp; [Pre-expansions](#pre-expansions)

&emsp; [Insert-expansions](#insert-expansions)

&emsp; [Post-expansions](#post-expansions)

##### &emsp;[Minimal-expansions](#minimal-expansions-label-definitions-link)


### [Dialogue Acts](#da-label-definitions-link)

##### &emsp;[Information-seeking Functions](#information-seeking-functions-label-definitions-link)

&emsp; [propositionalQuestion (Yes/No)](#propositionalquestion-yesno)

&emsp; [setQuestion (Who/What/Where/How)](#setquestion-whowhatwherehow)

&emsp; [choiceQuestion](#choicequestion)

&emsp; [checkQuestion](#checkquestion)

##### &emsp;[Information-providing Functions](#information-providing-functions-label-definitions-link)

&emsp; [inform (Statement)](#inform-statement)

&emsp; [answer](#answer)

&emsp; [agreement](#agreement)

&emsp; [disagreement](#disagreement)

&emsp; [correction](#correction)

&emsp; [confirm](#confirm)

&emsp; [disconfirm](#disconfirm)

##### &emsp;[Commissive Functions](#commissive-functions-label-definitions-link)

&emsp; [offer](#offer)

&emsp; [conditionalAccept (Consider/Address a Request/Suggestion/Offer)](#conditionalaccept-consideraddress-a-requestsuggestionoffer)

&emsp; [accept (Request/Suggestion/Offer)](#accept-requestsuggestionoffer)

&emsp; [decline (Request/Suggestion/Offer)](#decline-requestsuggestionoffer)

##### &emsp;[Directive Functions](#directive-functions-label-definitions-link)

&emsp; [request](#request)

&emsp; [suggest](#suggest)

##### &emsp;[Feedback Functions](#feedback-functions-label-definitions-link)

&emsp; [autoPositive (Positive Understanding/Feedback)](#autopositive-positive-understandingfeedback)

&emsp; [autoNegative (Negative Understanding/Feedback)](#autonegative-negative-understandingfeedback)

##### &emsp;[Time Management Functions](#time-management-functions-label-definitions-link)

&emsp; [stalling (Pausing)](#stalling-pausing)

##### &emsp;[Own and Partner Communication Management Functions](#own-and-partner-communication-management-functions-label-definitions-link)

&emsp; [retraction (Abandon)](#retraction-abandon)

##### &emsp;[Social Obligations Management Functions](#social-obligations-management-functions-label-definitions-link)

&emsp; [greeting](#greeting)

&emsp; [goodbye](#goodbye)

&emsp; [thanking](#thanking)

&emsp; [acceptThanking](#acceptthanking)

&emsp; [apology](#apology)

&emsp; [acceptApology](#acceptapology)


[Reference List](#references)
------------

Overview<a name="overview-link"></a>
========
The Conversation Analysis Modelling Schema (CAMS) defines a domain agnostic annotation scheme for dialogue that is aligned with relevant theories from within the CA literature and the Dialogue Act Mark-up Language (DiAML) as defined in ISO 24617 (British Standards Institution, 2012). The schema defines both Adjacency Pairs (AP) and Dialogue Acts (DA) which combine to form AP-types. The AP-type labels are designed to capture the semantic and syntactic structure of an interaction, in a format that is independent of the domain or topic, and which facilitate the computational modelling of dialogue.

There are 11 AP in the schema and the set includes; FPP and SPP for base, pre, post and insert-expansions as described by Liddicoat, (2007) and Sidnell, (2010). Because dialogue does not always contain even numbers of utterances, there are also single-labels (pre, post and insert) for utterances that do not belong to conventional AP. These are closely related to the idea of minimal-expansions (Schegloff, 2007), in that they are not designed to project any further sequences of talk, but rather open, close or add to sequences respectively.

The set of 27 DA are derived from the Dialogue Act Mark-up Language (DiAML) as defined in ISO 24617 (British Standards Institution, 2012). DiAML was developed as an empirically and theoretically well founded, application independent, DA annotation scheme and is also intended to be used by both human annotators and automatic annotation methods.

## Adjacency Pairs (AP)<a name="ap-overview-link">
AP are the base units of sequence-construction in talk, and in their basic unexpanded form comprise of two turns by different speakers that take place one after the other. The initial turn is called the First Pair Part (FPP) and initiates an exchange, the second turn is a Second Pair Part (SPP) which are responsive to the prior FPP. For example:

     A: Do you know the directions to the Zoo?          FPP-base

     B: Get on the subway.                              SPP-base

To account for more complex dialogue structures, AP also include the concept of expansion which allows the construction of sequences of talk that are made up of more than one AP, while still contributing to the same basic action, i.e. a question (FPP-base) could be followed by a question (FPP-insert), to elicit information required to better answer the initial question. For example:

     A: Do you know the directions to the Zoo?          FPP-base

        B: You driving or walking?                         FPP-insert

        A: Walking.                                        SPP-insert

     B: Get on the subway.                              SPP-base

## Dialogue Acts (DA)<a name="da-overview-link">
DA are a method of labelling the semantic content and communicative function of a single utterance of dialogue, such as, a question, request or greeting etc. The semantic content specifies objects, propositions and events that the DA is about; the communicative function specifies the way an addressee should use the semantic content to update their information, or dialogue, state (Bunt et al., 2012). For example, the propositional question “Do you know the directions to the Zoo?” contains a proposition (Do you know directions?) and an object (the Zoo). The addressee knows that a response is expected (communicative function) and can use this information (semantic content) to formulate a response.

     A: Do you know the directions to the Zoo?          propositionalQuestion
     
     B: Get on the subway.                              answer

## Adjacency Pair Types (AP-types)<a name="ap-types-overview-link">
AP can also be ‘type related’ and this pair-type relation has the useful property of limiting the range of possible responses to a given FPP. For example, a question could be followed by an answer, or followed by a question (FPP-insert), to elicit information required to better answer the initial question. Within CAMS the AP-types are defined by the addition of a DA label. Both the AP and DA labels are combined to create an AP-type label for each utterance of a dialogue.

     A: Do you know the directions to the Zoo?          FPP-base - proposotionalQuestion

        B: You driving or walking?                         FPP-insert - choiceQuestion

        A: Walking.                                        SPP-insert - answer

     B: Get on the subway.                              SPP-base - answer

AP then, can act as formal set of ‘rules’ which describe how an interaction can be structured and that apply to all types of conversation, irrespective of the current topic or objectives of the interaction. The inclusion of DA as semantic type-labels for adjacency-pair-parts support this structure, by enabling the identification and selection of subsequent pair-parts and capturing an exchange into a single structure (Boyer et al., 2009).

Annotation Guidelines<a name="annotation-guidelines-link">
=====================
The following section provides some guidance on the application of the schema when annotating dialogue and outlines certain limitations or restrictions that must be considered to maintain consistency with the definitions.

## Adjacency Pair Sequences<a name="ap-annotation-guidelines-link">
For all AP sequence-types; base, pre, insert and post expansions the following rules apply:

1.	The speaker of a FPP must be different to the speaker of a SPP.

2.	A FPP must be an initiation of a sequence and the SPP a response to that initiating FPP.

3.	Once a FPP has initiated a sequence, that sequence must be concluded with a SPP of the same type.

4.	The initiation and conclusion of two different sequences may not overlap each other. For example, the following is not permitted;

     Utterance 1		FPP-base
     
     Utterance 2			FPP-insert
     
     Utterance 3		SPP-base
     
     Utterance 4			SPP-insert

### Base Sequences
Once a FPP-base has initiated a sequence, that sequence must be concluded with a SPP-base before any further base-type sequences are initiated, i.e. a base-type sequence may not be ‘nested’ within another base-type sequence.

### Pre and Post Sequences
*Pre-expansions* and *Post-expansions* must be initiated and concluded prior to (Pre), or after (Post), any base-type sequence and are not permitted within base-type sequences, i.e. A *Pre-expansion* must be initiated and concluded prior to the initiation of a base-type sequence.

Once a FPP of type Pre or Post has initiated a sequence, that sequence must be concluded with a SPP of the same type before any further sequences of that type are initiated, i.e. a *Pre-expansion* sequence may not be ‘nested’ within another *Pre-expansion* sequence.

### Insert Sequences
*Insert-expansions* are the only expansions permitted within a base-type sequence, and they are not permitted outside of a base-type sequence, i.e. within a *Pre-expansion*.

Unlike base, pre and post type sequences, *Insert-expansion* are permitted to be ‘nested’, provided they abide by the usual constraints for AP, different speakers for FPP and SPP, not overlapping etc.

### Minimal Expansion
*Minimal-expansions* allow for additional turns that behave as expansions but consist only of one turn. Their primary role is to account for the uneven number of utterances in a dialogue, which is often the case, and single utterances that do not belong to a pair-sequence. For example, they allow the same speaker to produce more than one utterance of different types in succession or for a speaker to produce one utterance that does not belong to (initiate or conclude) an AP.

*Minimal-expansions* have fewer restrictions than pair-sequences to allow for flexibility when annotating. However, they should abide by their semantic intent. For example, a *pre-minimal-expansion* should be relating to a future base-type sequence, a *post-minimal-expansion* to a previous base-type sequence and an *insert-minimal-expansion* within a sequence.

## Dialogue Acts and Adjacency Pair Types (AP-types)<a name="da-ap-types-annotation-guidelines-link">
To produce AP-types an annotator must simply select one AP and one DA for an utterance of dialogue and the combination of these two labels is considered an AP-type label. The selection of the DA is dependent on the *semantic content* and *communicative function* of the individual utterance and the AP the utterances position within, or relation to, the structure of the dialogue.

Due to the large number of possible combinations, and to allow flexibility, the schema does not explicitly define all valid DA and AP combinations. Instead, annotators should consider the meaning and context within which the individual labels being applied to produce AP-types. The following should provide some guidance when selecting combinations of appropriate labels. However, while they should apply in many circumstances, these are only examples, not explicit rules:

- FPP are likely to have associated DA labels that are within the *Information-seeking* and *Directive* Function categories.

- SPP are likely to have associated DA labels that are within the *Information-providing* and *Commissive* Function categories.


Label Definitions<a name="label-definitions-link">
=================

## Adjacency Pairs<a name="ap-label-definitions-link">
Adjacency pairs are the basic units on which sequences in conversation are
built. Their core features are:

1.  Consist of two turns (utterances) by different speakers.

2.  Placed next to each other in basic (unexpanded) form, i.e. without an *expansion*.

3.  Are ordered, so that one always occurs after another. Initiation of a
    sequence is a *First Pair Part* (FPP) and the response *Second Pair Part* (SPP).

4.  Differentiated into AP-types. The relationship between FPP and SPP is
    constrained by the type of FPP produced i.e. a *question* followed by an *answer*.

Base<a name="base-label-definitions-link">
----
The basic sequence is composed of two ordered turns at talk, the FPP and SPP.
Participants in conversation orient to this basic sequence structure in
developing their talk and AP have a normative force in organizing conversation
,in that, AP set up expectations about how talk will proceed.

**Labels:** *FPP-base, SPP-base*

**Example:**

     A: What time is it?        FPP-base - setQuestion

     B: Three o’ clock.         SPP-base - answer

Expansions<a name="expansions-label-definitions-link">
----------
Expansion allow talk which is made up of more than a single AP to be constructed
and understood as performing the same basic action and the various additional
elements are seen as doing interactional work related to the basic action under
way. Sequence expansion is constructed in relation to a base sequence of a FPP
and SPP in which the core action under way is achieved.
There are three types of expansion pairs:

#### Pre-expansions
Pre-expansions are designed to be preliminary to some projected base sequence
and are hearable by participants as preludes to some other action.

**Labels:** *FPP-pre, SPP-pre*

**Example:**

     A: What you doing?         FPP-pre - setQuestion

     B: Not much.               SPP-pre - answer

        A: Wanna drink?             FPP-base - propositionalQuestion

        B: Sure.                    SPP-base - confirm

#### Insert-expansions
Insert-expansions occur between base adjacency pairs and separates the FPP and
SPP. Insert-expansions interrupt the activity previously underway but are still
relevant to that action and allows the second speaker (who must produce the base
SPP), to do interactional work relevant to the base SPP. Insert expansion is
realised through a sequence of its own and is launched by a FPP from the second
speaker which requires a SPP for completion. Once the sequence is completed the
base SPP once again becomes relevant as the next action.

**Labels:** *FPP-insert, SPP-insert*

**Example:**

     A: Do you know the directions to the Zoo?          FPP-base - propQuestion

        B: You driving or walking?                         FPP-insert - choiceQuestion

        A: Walking.                                        SPP-insert - answer

     B: Get on the subway.                              SPP-base - answer

#### Post-expansions
Sequences are also potentially expandable after the completion of the base SPP.
Once an SPP has been completed, the sequence is potentially complete: the action
launched by the FPP has run its course and a new action could appropriately be
begun. However, it is also possible for talk to occur after the SPP which is
recognizably associated with the preceding sequence. That is, it is possible for
sequences to be expanded after their SPP.

**Labels:** *FPP-post, SPP-post*

**Example:**

     A: What is the weather like today and tomorrow?     FPP-base - setQuestion

     B: Forecast for cloudy skies today.                 SPP-base - answer

        A: Okay.                                            FPP-post - autoPositive

        B: No problem.                                      SPP-post - acceptThanking

#### Minimal-expansions<a name="minimal-expansions-label-definitions-link">
Minimal-expansion involves the addition of one additional turn to a sequence.
The turn which is added is designed not to project any further within-sequence
talk beyond itself; that is, it is designed to constitute a minimal expansion
before, during or after the pair part. The primary role is to allow for
additional turns that behave as expansions but consist only of one turn.

**Labels:** *Pre, Insert, Post*

**Example:**

     A: My tooth hurts...                               Pre - inform

        A: When is my dentist appointment?                  FPP-base - setQuestion

            A: Who am I going with?                             Insert - setQuestion

        B: The appointment is at 11 am with your Aunt.      SPP-base - answer

            A: Thanks.                                           Post - thanking

## Dialogue Acts<a name="da-label-definitions-link">
An utterances DA describes not just its meaning, but the speakers intentions in the wider context of the conversation,  and therefore, facilitate the computational modelling of communicative behaviour in dialogue (Bunt et al., 2012). The following DA are aligned with DiAML (ISO 24617-2) (British Standards Institution, 2012) and are arranged into eight categories according to their function.

Information-seeking Functions<a name="information-seeking-functions-label-definitions-link">
-----------------------------

#### propositionalQuestion (Yes/No)
Communicative function of a dialogue act performed by the sender, S, in order to know whether the proposition, which forms the semantic content, is true. S assumes that A knows whether the proposition is true or not and puts pressure on A to provide this information.

A propositional question corresponds to what is commonly termed a YN-question in the linguistic literature. This standard prefers the term ‘propositional question’ because the term ‘YN-Question’ carries the suggestion that this kind of question can only be answered by ‘yes’ or ‘no’, which is not the case.

**Example:** “Does the meeting start at ten?”

#### setQuestion (Who/What/Where/How)
Communicative function of a dialogue act performed by the sender, S, in order to know which elements of a given set have a certain property specified by the semantic content; S puts pressure on the addressee, A, to provide this information, which S assumes that A possesses. S believes that at least one element of the set has that property.

A set question corresponds to what is commonly termed a WH-question in the linguistic literature. The term ‘set question’ is preferred because: (a) it clearly separates form from function by removing any oblique reference to syntactic criteria for the identification of such acts; and (b) it is not a language specific term (it may be further noted that even in English, not all questioning words begin with ’wh’, e.g. “How?”).

**Example:** “What time does the meeting start?”; “How far is it to the station?”

#### choiceQuestion
Communicative function of a dialogue act performed by the sender, S, in order to know which one from a list of alternative propositions, specified by the semantic content, is true; S believes that exactly one element of that list is true; S assumes that the addressee, A, knows which of the alternative propositions is true, and S puts pressure on A to provide this information.

It is not very common in annotation schemes to specifically distinguish the concept of choice questions from that of set questions. However, whereas it is common for the concept set question to carry the expectation that all members of the set with a given property should be returned by the addressee, for a choice-question the expectation is that there will be exactly one. The different preconditions and effects indicate that these are semantically different concepts, and they have been treated here as such.

**Example:** “Should the telephone cable go in telephone line or in external line?”

#### checkQuestion
Communicative function of a dialogue act performed by the sender, S, in order to know whether a proposition, which forms the semantic content, is true, S holds the uncertain belief that it is true S. S assumes that A knows whether the proposition is true or not and puts pressure on A to provide this information.

**Example:** “The meeting starts at ten, right?”

Information-providing Functions<a name="information-providing-functions-label-definitions-link">
-------------------------------

#### inform (Statement)
Communicative function of a dialogue act performed by the sender, S, in order to make the information contained in the semantic content known to the addressee, A; S assumes that the information is correct.

The inform function may also have more specific rhetorical functions such as: explain, elaborate, exemplify and justify; this is treated in this standard by means of rhetorical relations.

**Example:** “The 6.34 to Breda leaves from platform 2.”

#### answer
Communicative function of a dialogue act performed by the sender, S, in order to make certain information available to the addressee, A, which S believes A wants to know; S assumes that this information is correct.

**Example:**

S: “what does the display say?”

A: “Send error document ready.”

#### agreement
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A that S assumes a given proposition to be true, which S believes that A also assumes to be true.

DAMSL and SWBD-DAMSL use “Agreement” to refer to various degrees in which some previous proposal, plan, opinion or statement is accepted; “accept” is one of these degrees; “reject” is another.

**Example:** “Exactly.”

#### disagreement
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A that S assumes a given proposition to be false, which S believes that A assumes to be true.

DAMSL and SWBD-DAMSL use “Agreement” to refer to various degrees in which a speaker accepts some previous proposal, plan, opinion or statement; “accept” is one of these degrees; “reject” is another.

**Example:**

S: “Do you know where to find the ink cartridge?”

A: “Oh I think to the left of the paper.”

S: “Uh... no.”

#### correction
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A, that certain information which S has reason to believe that A assumes to be correct, is in fact incorrect and that instead the information that S provides is correct.

**Example:** “To Montreal, not to Ottawa.”

#### confirm
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A, that certain information that A wants to know, and concerning which A holds an uncertain belief, is indeed correct.

**Example:** “Indeed.”

#### disconfirm
Communicative function of a dialogue act performed by the sender, S, in order to let the addressee, A, know that certain information that A wants to know, and concerning which A holds an uncertain belief, is incorrect.

**Example:** “Nope.”

Commissive Functions<a name="commissive-functions-label-definitions-link">
--------------------

#### offer
Communicative function of a dialogue act by which the sender, S, indicates their willingness and ability to perform the action, specified by the semantic content, conditional on the consent of addressee A that S do so.

**Example:** “I will look that up for you.”

#### conditionalAccept (Consider/Address a Request/Suggestion/Offer)
Communicative function of a dialogue act by which the sender, S, indicates that they will consider the performance of an action, depending on certain conditions that they make explicit. The action may be one that they were requested to perform or was suggested that they perform. Or to indicate that they are considering the possibility that the addressee, A, performs the action that A has previously offered to perform.

The conditionalAccept function covers a range of possible responses to a request, suggestion or offer. If the condition specified is met the sender commits to the action, or accepts the offer, otherwise the sender in fact declines to perform the requested action or accept the offer.

**Example:**

A: “Please give me the gun.”

S: “If you push the bag to me.”

#### accept (Request/Suggestion/Offer)
Communicative function of a dialogue act by which the sender, S, commits them self to perform an action that they have been requested to perform or was suggested that they perform. Or to inform the addressee, A, that S would like A to perform the action that A has previously offered to perform.

**Example:**

A: “Would you like help with that?”

S: “Sure.”

#### decline (Request/Suggestion/Offer)
Communicative function of a dialogue act by which the sender, S, indicates that they refuse to perform an action that they have been requested to perform or was suggested that they perform. Or to inform the addressee, A, that S does not want A to perform the action that A has previously offered to perform.

**Example:**

A: “Would you like help with that?”

S: “No thank you.”

Directive Functions<a name="directive-functions-label-definitions-link">
-------------------

#### request
Communicative function of a dialogue act performed by the sender, S, in order to create a commitment for the addressee, A, to perform a certain action in the manner or with the frequency described by the semantic content, conditional on A’s consent to perform the action. S assumes that A is able to perform this action.

**Example:** “Please turn to page five”; “Please don’t do this ever again”;
“Please drive very carefully”.

#### suggest
Communicative function of a dialogue act performed by the sender, S, in order to make the addressee, A, consider the performance of a certain action, specified by the semantic content, S believes that this action is in A’s interest, and assumes that A is able to perform the action.

**Example:** “Let’s wait for the speaker to finish.”

Feedback Functions<a name="feedback-functions-label-definitions-link">
------------------

#### autoPositive (Positive Understanding/Feedback)
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A that S believes that S’s processing of the previous utterance(s) was successful.

Feedback mostly concerns the processing of the last utterance from the addressee, but sometimes, especially in the case of positive feedback, it concerns a longer stretch of dialogue.

**Example:** “Uh-huh”; “Okay”; “Yes”

#### autoNegative (Negative Understanding/Feedback)
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A that S’s processing of the previous utterance(s) encountered a problem.

**Example:** “Sorry?”; “What?”

Time Management Functions<a name="time-management-functions-label-definitions-link">
-------------------------

#### stalling (Pausing)
Communicative function of a dialogue act performed by the sender, S, in order to have a little extra time to construct their contribution or to suspend the dialogue for a short while.

Pausing occurs either in preparation of continuing the dialogue, or because something else came up which is more urgent for the sender to attend to.

**Example:** “Let me see...”; “Ehm...”; “Just a moment”; “Umm...”

Own and Partner Communication Management Functions<a name="owne-and-partner-communication-management-functions-label-definitions-link">
--------------------------------------------------

#### retraction (Abandon)
Communicative function of a dialogue act performed by the sender, S, in order to withdraw or abandon something that they just said within the same turn.

**Example:** “Then we’re going to g– ”

Social Obligations Management Functions<a name="social-obligations-management-functions-label-definitions-link">
---------------------------------------

#### greeting
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A that S is present and aware of A’s presence.

Greetings usually come in initiative-response pairs and are commonly used to open a dialogue.

**Example:** “Hello!”; “Good morning”

#### goodbye
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A, that S intends the current utterance to be their final contribution to the dialogue.

Goodbyes usually come in initiative-response pairs and are commonly used to close a dialogue.

**Example:** “Bye bye, see you later.”

#### thanking
Communicative function of a dialogue act performed by the sender, S, in order to inform the addressee, A, that S is grateful for some action performed by A; S puts pressure on A to acknowledge this.

Utterances used for thanking often also indicate that the sender wants to end the dialogue.

**Example:** “Thanks a lot.”

#### acceptThanking
Communicative function of a dialogue act performed by the sender, S, in order to mitigate to the feelings of gratitude which the addressee, A’, has expressed.

**Example:** “Don’t mention it.”

#### apology
Communicative function of a dialogue act performed by the sender, S, in order to signal that they want the addressee, A, to know that S regrets something; S puts pressure on A to acknowledge this.

**Example:** “Sorry about that.”

#### acceptApology
Communicative function of a dialogue act performed by the sender, S, in order to mitigate, the feelings of regret that the addressee, A, has expressed.

**Example:** “No problem.”

References
==========

Boyer, K.E., Ha, E.Y., Phillips, R., Wallis, M.D., Vouk, M.A. and Lester, J. (2009) Inferring Tutorial Dialogue Structure with Hidden Markov Modeling. In: Proceedings of the Fourth Workshop on Innovative Use of NLP for Building Educational Applications - EdAppsNLP ’09 [online]. 2009 pp. 19–26. Available from: https://www.cs.rochester.edu/~tetreaul/bea4/Boyer-BEA4.pdfdoi:10.3115/1609843.1609846 [Accessed 18 November 2017].

British Standards Institution (2012) ISO 24617-2: Language Resource Management - Semantic Annotation Framework (SemAF) Part 2: Dialogue acts [online]. Available from: https://bsol-bsigroup-com.

Bunt, H., Alexandersson, J., Choe, J.-W., Fang, A.C., Hasida, K., Petukhova, V., Popescu-belis, A. and Traum, D. (2012) ISO 24617-2 : A Semantically-based Standard for Dialogue Annotation. In: Proceedings of LREC 2012 [online]. 2012 pp. 430–437. Available from: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.381.2726&rep=rep1&type=pdf [Accessed 16 November 2017].

Liddicoat, A.J. (2007) An Introduction to Conversation Analysis.  London: Continuum.

Schegloff, E.A. (2007) Sequence Oranization in Interaction: A Primer in Conversation Analysis I [online]. Cambridge: Cambridge University Press. [Accessed 17 November 2017].

Sidnell, J. (2010) Conversation Analysis - An Introduction [online]. (no place) Whiley-Blackwell. [Accessed 8 January 2018].


