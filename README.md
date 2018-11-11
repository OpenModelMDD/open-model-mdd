# open-model-mdd
A discrete event simulation model to assess the cost-effectiveness of alternative treatment strategies for patients with Major Depressive Disorder (MDD).

# Major Depressive Disorder
Major depressive disorder (MDD) is a complex public health problem associated with significant medical, social and economic burden. MDD lifetime prevalence ranges from 10 to 15%[1]. The disease remains highly recurrent despite therapeutic progress[2] and is associated with a risk of suicide over 20 times higher than in the general population[3]. In 2004, the total costs of MDD reached $118 billion in Europe, with 36% of outpatient care and drug costs, 8% of hospitalization costs and 64% of indirect costs resulting from lost productivity and mortality[4]. MDD is predicted to become the second leading contributor to the world´s disease burden by 2020[5].

# Existing economic models
There is a large number of antidepressant drugs on the market; for instance 27 in the British National Formulary, with different efficacy and tolerability profiles, as well as different costs. In that context, a cost-effectiveness model would be useful to inform the choice between alternative treatment strategies.
Decision trees models (DT) have been applied to assess the cost-effectiveness of MDD treatments. They have a main limitation of being inflexible to cover the disease´s long term events[6]. Events such as recurrence and their corresponding health states are missed by DT as the model time horizon covers only the acute phase of depression, although treatment continues after remission to prevent relapse. Representing these missed events is technically possible within the DT models. However this would result in broadening the number of corresponding health states.
The use of a Markov model is another option. However simple Markov models lack memory[7] as they do neither consider previous depressive episodes nor previously received treatments. Tracking treatment history would necessitate broadening the number of health states which, as in DTs, may impede the model implementation and analysis, or using patient-level simulation[6].

# A new economic model for MDD
MMD model structure
The discrete-event simulation (DES) approach overcomes these limitations of this decision trees or simple Markov models and is more flexible and less computing intensive than Markov models running at patient level[8]. DES models conceptualize the course of patients in terms of experienced events and their impact on current and future health, medical resource use and other components, continuously in time, while allowing chance to play a role. Patient characteristics, so-called attributes, which influence events´ occurrence, can be updated accordingly.
This model simulates short- and long-term clinical events (partial response, remission, relapse, recovery, recurrence), adverse events, and treatment changes (titration, switch, addition, discontinuation) in a cohort of MDD patients over up to 5 years. Patient characteristics influencing clinical evolution are considered (e.g., residual symptoms). It can be used to predict costs and quality-adjusted life-years (QALYs) associated with alternative treatment strategies in MDD.
The current version of the model was populated with data for fictitious antidepressants with three levels of efficacy, tolerability and drug cost (low, medium, high) from first-line to third-line. Unit costs for the UK have been entered. However, these input data can be used for the purpose of testing the model only. The results that you will obtain by running the provided set of input data are not intended to reflect the cost-effectiveness of any actual treatment strategy.
This model was developed in Scilab. Scilab is a widely used open-source computer program for numerical computation for industry, education and research.

#Reference:
Toumi M, Antonanzas F, Hakkaart L, Lam RW, McCrone P, Persson U, Vataire AL and Aballéa S. Comprehensive discrete event simulation model for the evaluation of health care technologies in depression.
Presented at ISPOR 15th Annual European Congress, November 2012, Berlin, Germany

[1] Lepine JP, Briley M. The increasing burden of depression. Neuropsychiatr Dis Treat 2011;7(Suppl 1):3-7.
[2] Jan Scott, Barbara Dickey. Global burden of depression: the intersection of culture and medicine. The British Journal of Psychiatry , 121-131. 2003.
[3] Osby U, Brandt L, Correia N, et al. Excess mortality in bipolar and unipolar disorder in Sweden. Arch Gen Psychiatry 2001 Sep;58(9):844-50.
[4] Sobocki P, J&ouml;nsson B, Angst J, Rehnberg C. Cost of depression in Europe. J Ment Health Policy Econ. 2006 Jun;9(2):87-98.
[5] Ostin TB, Ayuso-Mateos JL, Mathers C. Global burden of depressive disorders in the year 2000. The British Journal of Psychiatry 184, 386-392. 2004.
[6] Haji Ali AH, Karnon J, Gray J. A critical review of model-based economic studies of depression: modelling techniques, model structure and data sources. Pharmacoeconomics 2012 Jun 1;30(6):461-82.
[7] Klein RW, Dittus RS, Roberts SD, Wilson JR. Simulation modeling and health-care decision making. Med Decis Making 1993 Oct;13(4):347-54.
[8] Le Lay A, Despiegel N, Fran&ccedil;ois C and Duru G. Can discrete event simulation be of use in modelling major depression? Cost Effectiveness and Resource Allocation 2006 Dec, 4:19.
