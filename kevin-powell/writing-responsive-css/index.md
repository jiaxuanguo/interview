#[Are you writing responsive CSS the wrong way?](https://www.youtube.com/watch?v=0ohtVzCSHqs)
1. consider designing websites mobile-first
2. set ```margin-right: auto; margin-left: auto;``` to center an element; furthermore, set these two rules on **two different elements** to center everything in between
3. the main argument is that mobile layout is usually simpler, 
making it a better starting point
4. a single column layout with block elements stacking beneath one another is responsive by default
5. create columns without using flex or grid - multi-column layout
6. set a fixed column width to achieve response column counts
