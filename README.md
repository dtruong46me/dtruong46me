<a name="main-py"></a>
**`main.py`**

<pre>
<i>"""
Hi, you found my GitHub profile.

Click any function name to jump to its definition.
Open "Run" below to see what it prints.
"""</i>

<b>from</b> <a href="#humans-py">humans</a> <b>import</b> <a name="import-dinhtruongphan" href="#class-dinhtruongphan">DinhTruongPhan</a> <b>as</b> <a name="import-dinhtruong" href="#class-dinhtruongphan">DinhTruong</a>


<b>def</b> <b><a name="def-main">main</a></b>():
    me = <a href="#class-dinhtruongphan">DinhTruong</a>()

    intro    = me.<a name="call-overview" href="#def-overview">overview</a>()
    today    = me.<a name="call-currently" href="#def-currently">currently</a>()
    history  = me.<a name="call-changelog" href="#def-changelog">changelog</a>()
    tools    = me.<a name="call-tech_stack" href="#def-tech_stack">tech_stack</a>()
    work     = me.<a name="call-projects" href="#def-projects">projects</a>()
    offline  = me.<a name="call-hobbies" href="#def-hobbies">hobbies</a>()
    writing  = me.<a name="call-blog" href="#def-blog">blog</a>()
    links    = me.<a name="call-contact" href="#def-contact">contact</a>()

    me.<a name="call-diary" href="#def-diary">diary</a>()  <i># go ahead, try it</i>


<b>if</b> __name__ == "__main__":
    <a href="#def-main">main</a>()
</pre>

<details>
<summary><b>Run</b>&nbsp;&nbsp;<code>$ python main.py</code></summary>

```console
$ python main.py
Dinh Truong Phan
AI Engineer at [Company].
I build LLM systems, and the unglamorous
infrastructure that keeps them alive in production.

currently
---------
  working on  [agents / RAG / inference serving]
  exploring   speech (ASR, TTS)

changelog
---------
  v0.1  [2021]  Started Data Science & AI at HUST
  v0.5  [2024]  Intern at [ABC], [what you did]
  v1.0  [2025]  Graduated
  v1.1  [2025]  Joined [Company] as AI Engineer
  v2.0  [20xx]  [Moved to Japan / new job / ...]

tech stack
----------
  Python, PyTorch, Hugging Face, LangGraph, Docker, Kubernetes, AWS

projects
--------
  [project-name]    one line on what it does
  [project-name]    ...
  more, including the ones that went nowhere: me.blog()

hobbies
-------
  [piano / guitar], Japanese, English, [...]

blog
----
  Coder thích chơi đàn
  a coder who likes to play music:
  projects, experiments, half-serious ideas,
  notes from learning English and Japanese

contact
-------
  github  github.com/dtruong46me
  blog    [blog-url]
  email   [email]
Traceback (most recent call last):
  File "main.py", line 27, in <module>
    main()
  File "main.py", line 23, in main
    me.diary()  # go ahead, try it
  File "humans.py", line 93, in diary
    raise PermissionError("private. nice try.")
PermissionError: private. nice try.
```

</details>

<a name="humans-py"></a>
**`humans.py`**

<pre>
<i>"""
humans.py

One of them, anyway.
"""</i>


<b>def</b> <b><a name="def-section">section</a></b>(title):
    print(f"\n{title}")
    print("-" * len(title))


<b>class</b> <b><a name="class-dinhtruongphan" href="#import-dinhtruongphan">DinhTruongPhan</a></b>:
    <i>"""AI Engineer. A coder who likes to play music."""</i>

    name = "Dinh Truong Phan"
    github = "github.com/dtruong46me"

    <b>def</b> <b><a name="def-overview" href="#call-overview">overview</a></b>(<b>self</b>):
        print(<b>self</b>.name)
        print("AI Engineer at [Company].")
        print("I build LLM systems, and the unglamorous")
        print("infrastructure that keeps them alive in production.")
        <b>return</b> <b>self</b>.name

    <b>def</b> <b><a name="def-currently" href="#call-currently">currently</a></b>(<b>self</b>):
        now = {
            "working on": "[agents / RAG / inference serving]",
            "exploring": "speech (ASR, TTS)",
        }
        <a href="#def-section">section</a>("currently")
        <b>for</b> what, detail <b>in</b> now.items():
            print(f"  {what:&lt;12}{detail}")
        <b>return</b> now

    <b>def</b> <b><a name="def-changelog" href="#call-changelog">changelog</a></b>(<b>self</b>):
        history = [
            ("v0.1", "[2021]", "Started Data Science &amp; AI at HUST"),
            ("v0.5", "[2024]", "Intern at [ABC], [what you did]"),
            ("v1.0", "[2025]", "Graduated"),
            ("v1.1", "[2025]", "Joined [Company] as AI Engineer"),
            ("v2.0", "[20xx]", "[Moved to Japan / new job / ...]"),
        ]
        <a href="#def-section">section</a>("changelog")
        <b>for</b> version, year, event <b>in</b> history:
            print(f"  {version:&lt;6}{year:&lt;8}{event}")
        <b>return</b> history

    <b>def</b> <b><a name="def-tech_stack" href="#call-tech_stack">tech_stack</a></b>(<b>self</b>):
        stack = ["Python", "PyTorch", "Hugging Face", "LangGraph",
                 "Docker", "Kubernetes", "AWS"]
        <a href="#def-section">section</a>("tech stack")
        print("  " + ", ".join(stack))
        <b>return</b> stack

    <b>def</b> <b><a name="def-projects" href="#call-projects">projects</a></b>(<b>self</b>):
        work = [
            ("[project-name]", "one line on what it does"),
            ("[project-name]", "..."),
        ]
        <a href="#def-section">section</a>("projects")
        <b>for</b> title, what <b>in</b> work:
            print(f"  {title:&lt;18}{what}")
        print("  more, including the ones that went nowhere: me.blog()")
        <b>return</b> work

    <b>def</b> <b><a name="def-hobbies" href="#call-hobbies">hobbies</a></b>(<b>self</b>):
        things = ["[piano / guitar]", "Japanese", "English", "[...]"]
        <a href="#def-section">section</a>("hobbies")
        print("  " + ", ".join(things))
        <b>return</b> things

    <b>def</b> <b><a name="def-blog" href="#call-blog">blog</a></b>(<b>self</b>):
        <a href="#def-section">section</a>("blog")
        print("  Coder thích chơi đàn")
        print("  a coder who likes to play music:")
        print("  projects, experiments, half-serious ideas,")
        print("  notes from learning English and Japanese")
        <b>return</b> "[blog-url]"

    <b>def</b> <b><a name="def-contact" href="#call-contact">contact</a></b>(<b>self</b>):
        links = {
            "github": <b>self</b>.github,
            "blog": "[blog-url]",
            "email": "[email]",
        }
        <a href="#def-section">section</a>("contact")
        <b>for</b> where, address <b>in</b> links.items():
            print(f"  {where:&lt;8}{address}")
        <b>return</b> links

    <b>def</b> <b><a name="def-diary" href="#call-diary">diary</a></b>(<b>self</b>):
        <b>raise</b> PermissionError("private. nice try.")
</pre>

[blog](https://your-blog-url) · [email](mailto:you@example.com) · [LinkedIn](https://linkedin.com/in/your-handle)
