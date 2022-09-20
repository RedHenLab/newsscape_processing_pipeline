# newsscape_processing_pipeline
This is the pipeline based on the research in Peter Uhrig's thesis - updated as needed

This pipeline assumes as starting points the NewsScape text file and the NewsScape video file

Processing Steps
- Where exactly? - Data quality assessment step 1
-- spell checking
-- audio signal quality check
-- video error check
- Sentence splitting (includes transformation of turn and story boundaries - extend to commercials?
- ToDo: Where do we incorporate the information about commercials? Either here or before/during sentence splitting.
- Extraction of non-spoken text
- Run CoreNLP
-- tokenization
-- pos
-- lemma
-- TrueCase
-- dependency parsing
-- NER
-- coreference resolution
- (optional) Run PathLSTM for semantic frame annotation
- Verticalize (including XML parsing to check integrity)
- Create input for Gentle
- Run Gentle (modified version!)
- Integrate Gentle results ToDo: FIX THIS!
- Data quality assessment step 2 - audio annotation quality (based on Gentle)
- Audio annotation with gender detection
- Run OpenPose and other image annotation software on video
- Integrate results
- In the long run: biometric, yolo, etc.
