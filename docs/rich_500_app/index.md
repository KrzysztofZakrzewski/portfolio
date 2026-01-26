# the_500_richest – application based on a previous analysis

I decided to revisit and refresh one of my older codebases.
It is a simple application used to present data from a previous analysis:

<a href="https://krzysztofzakrzewski.github.io/portfolio/rich_500/">rich_500</a>.

### The analysis itself is not the main focus of this presentation — the refactoring process is.

This is also the first application I have deployed to a production environment on my own server (Raspberry Pi 5 running Ubuntu Server 24.04 LTS), using Docker and Cloudflare.

### Refactoring Assumptions:

- Refactored a monolithic application (1,793 lines in a single file with heavy if/else logic) into a modular structure.

- Reduced the main application file to ~60 lines by extracting responsibilities into separate modules.

- Introduced 12 new files to improve separation of concerns and maintainability.

- Although the total line count increased to ~1,865 lines, a significant portion consists of comments, spacing, and documentation.

- The effective amount of executable code was reduced to approximately 1,000 lines, with further optimization still possible.

- The resulting code base is much more readable, easier to maintain and extend than before. 😄

![screenshot](media/the500.png)

### Architecture

```
app/
│
├── app.py                  # entry point (Streamlit)
│
├── loader/
│   └── csv_loader.py           # load danych
|
├── data/
│   └──top_rich2024_ready.csv   # csv data
|
├── analysis/
│   ├── data_overwview.py       # universal compiuting for basic data overview
│   ├── statistics_for_countries.py # descriptive statistics for countrys analysis
│   └── statistics_for_global.py    # descriptive statistics for global analysis
│
│
├── visualization/
│   ├── plots.py            # plots for global analysis
│   └── plots_countrys.py   # plots for countrys analysis
│
├── ui/
│   ├── components          # sidebar global an countrys
|   |   └── data_overview.py  # render universal view for basic data overview
|   |
│   ├── sidebar.py          # sidebar uniwersal for all        
│   ├── components.py          # sidebar uniwersal for all        
|   |   |
|   |   └── data_overview.py   # basic overview for global and coutrys analysis
|   |
│   ├── pages.py/           # page/tab logic
│   |   |
│   |   ├── about.py        # Descryption of app
|   |   ├── global_analis.py    # global analysis
│   |   ├── about.py        # Descryption of app
|   |   └── countrys.py     # anasysis for countrys
|   |
|   └──styles.py            # Css style for all app
|
│
└── requirements.txt
```

**Created 20.01.2026**

<a href="https://ritchproject.com/" download class="md-button md-button--primary">App link</a>

All changes were implemented based on the original dataset without altering their values or substantive content.

The changes included:

Converting numeric values written in shorthand (e.g., "447B") into readable numeric formats to facilitate calculations and readability.

Removing unnecessary spaces from column names to simplify work.

No DataFrame altered the original values.

## Author of orginal dataset:

<a href="https://www.kaggle.com/mahmoudredagamail/datasets" download class="md-button md-button--primary">Author of dataset</a> 
<a href="https://www.kaggle.com/datasets/mahmoudredagamail/the-worlds-500-most-powerful-businessmen" download class="md-button md-button--primary">Orginal Dataset</a>
<a href="data/top_rich2024_ready.csv" download class="md-button md-button--primary">Changed Dataset</a>

<script>
function resizeIframeToFitContent(iframe) {
    iframe.style.height = (iframe.contentWindow.document.documentElement.scrollHeight + 50) + "px";
    iframe.contentDocument.body.style["overflow"] = 'hidden';
}
window.addEventListener('load', function() {
    var iframe = document.getElementById('content');
    resizeIframeToFitContent(iframe);
});
window.addEventListener('resize', function() {
    var iframe = document.getElementById('content');
    resizeIframeToFitContent(iframe);
});
</script>