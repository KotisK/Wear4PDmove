# Wear4PDmoveOnto

**Ontology aim/scope:**

Wear4PDmoveOnto aims to semantically integrate heterogeneous data such as dynamic/stream data  (collected from wearables) and static/historic data (stored in PHR databases), in order to represent personal health knowledge in the form of a KG (i.e., PHKG), supporting health apps’ reasoning capabilities for high-level events recognition (e.g., ‘missing dose’ or  ‘patient fall’ event).

**Ontology requirements (briefly):** 

The ontology must:

R1.Represent knowledge about a) patients’ movement b) patients’ daily activities, c) details of their personal health record.

R2.Semantically integrate data from heterogeneous sources a) wearables, b) personal health records, in order to provide a unified view of personal health in real-time (monitoring and alerting).

R3.Reason with unified personal health data represented in the form of a KG.

R4.Support high-level events recognition in the personal health domain for PD, such as a ‘missing dose’ event or a ‘patient fall’ event.

**Example scenario (missing dose):**

Current pill dosing monitoring and alerting for PDs are using fixed time alerts (sound or/and messages) on smart phones/tablets, which are based on DDI values entered by patients or their doctors in the configuration settings of their apps. However, this approach does not consider the real/current status of patients’ health conditions, depending only on the actions taken by the application’s user i.e., the patient. Thus, the user-patient may always confirm the dosing (reception) at any time, moving away from the actual treatment plan (several times). To avoid this situation, the scenario implements an edge-device-based application that collects and analyses personal health data of PD patients in real-time (or close to real-time), trying to recognize an event of a missing dose by analyzing the combination of symptoms (low-level events) such as Bradykinesia (Slowness of Movement) and tremor of PD patients.

**examples, ontology and Protege 5.5**

To test the populated ontology and SWRL rules (for the example scenario), PMDO is also needed (provided in the .zip file) and the use of Pellet reasoner. Snap SPARQL plugin is needed for querying the inferred knowledge (triples) using SPARQL.
