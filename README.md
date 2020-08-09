# DepthSearch
**A tool to Ctrl+F a keyword not just in the current webpage, but in all the links of this page (..and so on recursively).**

> Terms:
>* Depth=0 : Regular current (home) page search
>* Depth=1 : Search through all pages linked in the home page
>* Depth=2 : Search through all pages linked in the all the pages that are linked to the home page
>* ...

Can have applications for those involved in research (scientists, journalists etc). Search through all the citations, mentions and hyperlinks easily.

The concern is the O(n^2) time complexity. 

This is best suited for Depth=1. Depths>=2 can take very long to be searched.

> **My observation:**
>1. News articles have average.. links
>2. Wikipedia has average.. citations
>3. Research papers have average..citations

## Next steps:
* PDF compatibility (for research papers)
* *Add an ad checker?* https://github.com/notracking/hosts-blocklists This list is so large that I need to compare (execution time of actually searching through ad URL) vs (finding URL in list of 2-4lakh ad domains) 
* If counting is not too expensive, first get all count?
* Collect all dictionaries into a final data structure instead of printing at each iteration

### How to reduce time ?
* Open the URL only once (instead of once for searching for links within and once for finding matchs)
* Dive deeper only in URLs that have non-zero matches

</br></br></br>
*Wanted this to be a browser extension. But given that time taken can be more than a minute for even depth=1, this will need to be reevaluated*
