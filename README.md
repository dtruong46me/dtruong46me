```
>>> from hust.alumni import DinhTruong
>>> me = DinhTruong()

>>> me.overview()
AI Engineer at [Company].
I build LLM systems, and the unglamorous
infrastructure that keeps them alive in production.

>>> me.currently()
{
    "working_on": "[agents / RAG / inference serving]",
    "learning":   ["speech (ASR/TTS)", "Japanese"],
    "playing":    "[piano / guitar]",
}

>>> me.changelog()
v1.1  (2026)  [Một việc thật ở công ty]
v1.0  (2025)  Graduated HUST, Data Science & AI.
              Thesis on [topic].
v0.x          Broke a lot of notebooks.
              Learned from most of them.

>>> me.beliefs()
- Evals before vibes.
- A model nobody can deploy is just a research paper.
- Most "LLM bugs" are data bugs in disguise.

>>> me.tech_stack()
{
    "ml":    ["Python", "PyTorch", "Hugging Face", "LangGraph", "Qdrant"],
    "infra": ["Docker", "Kubernetes", "ArgoCD", "MLflow"],
    "cloud": ["AWS"],
}

>>> me.projects()
[project-name]   one line on what it does
[project-name]   ...
# more (and the ones that went nowhere): me.blog()

>>> me.blog()
'Coder thích chơi đàn'   # a coder who likes to play music
# projects, experiments, half-serious ideas,
# notes from learning English and Japanese

>>> me.diary()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
PermissionError: private. nice try.
```
