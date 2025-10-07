# fan_fiction
FANFICTION GENERATOR 


1. Problem Definition: 
This is an NLP project, which is created to provide fanfiction lovers with a set of fanfiction that is generated based on emotion-lore match. We have realized that there are not many tools that provide readers with an exact emotion-lore match for a fun fanfiction experience, and this is what inspired us for this project. Our generator uses a data set of emotions (e.g positive, negative, happy) and generates the fanfiction content based on this set. 


2. This project aims to:


* prevent unmatching emotional tones based to the user’s interest and mood


* reduce time for searching for a related emotion and make lore-faithful fanfiction accessible for everyone


* We want to address that our texts are not logically consistent and only have syntactic/grammatical clearness. To improve that, we should use RNN, however; because of our busy schedule with the finals, we could not spend so much time on it and learn it well. (This stays as an area of improvement for the future of our project.) So we decided to improve the clean up section and the readability of the existing code. 
      
3. Project Management:
     
* I, Helin, want to state that Alena has significant experience in coding and big thanks to her for her help with the coding part of this project-her additional ideas on the evaluation were great too. We have come up with this idea after our class with N-Grams.She managed to work on the mistakes our code has and develop them further. I have tried my best with analyzing our project: what we are trying to provide with this project and how we can evaluate it. We are willing to work on our project further and improve it together.  
Core Development Roles

Role
Contributor
Responsibilities
	Prototype Developer
	Helin B.
	Designed and implemented the initial codebase, wrote core documentation.
	Feature Engineer
	Alena N.
	Enhanced the codebase, integrated new features (e.g., LLM-based improvements).
	Data & Evaluation Roles
Role
Contributor
Responsibilities
	Data Researcher
	Both
	Identified and sourced relevant databases on kaggle.com.
	Data Preprocessing Specialist
	Both
	Cleaned, formatted, and prepared datasets for use.
	Evaluation Architect
	Both
	Designed testing/evaluation methodologies.
	



4. Tasks and Tools Used:


Key Components
- Text preprocessing
- Learning from corpora (N-Grams)
- Text generation


Workflow


1. Data Acquisition
- Source text: "Lord of the Rings" (primary corpus[1])
- Additional datasets: HappyDB[2], Steam_Reviews[3] (emotion-based texts)


2. Preprocessing
- Cleaned raw text for improved readability
- Used spaCy for advanced text normalization (based on lemmatization, stopword removal, etc.)
- Split emotion-based texts into categorized files:
  - positive.txt
  - negative.txt
  - happy.txt


3. Model Training
- Built a 4-gram language model from the cleaned corpus
- Implemented two sampling methods:
  - Top-k sampling
  - Top-p (nucleus) sampling


4. Output Generation
- Generated texts saved to: evaluation_generated_texts.txt
- Includes outputs from:
  - LOTR-based generation
  - Emotion-tagged generation (positive/negative/happy)


File Structure
- /data/
  - raw/
    - urlopen (Lord of the Ring)
    - output_hb.csv (HappyDB)
    - output_steam.csv (Steam_Reviews: positive, negative)
  - processed/
    - clean_output_hb.csv
    - clean_output_steam.csv
    - positive.txt
    - negative.txt
    - happy.txt
- /outputs/
  - evaluation_generated_texts.txt


Dependencies


This project requires the following Python packages:


- `re` (Python built-in library)
- `nltk` (Natural Language Toolkit)
- `scipy` (for statistical operations)
- `numpy` (for numerical computations)
- `spacy` (for advanced NLP processing)
- `groq` (Groq API client)


Installation


You can install all required dependencies using pip:


```bash
pip install nltk scipy numpy spacy groq






________________
[1]https://archive.org/stream/tolkien-j.-the-lord-of-the-rings-harper-collins-ebooks-2010/Tolkien-J.-The-lord-of-the-rings-HarperCollins-ebooks-2010_djvu.txt
[2] https://www.kaggle.com/datasets/ritresearch/happydb
[3] https://www.kaggle.com/datasets/filipkin/steam-reviews
