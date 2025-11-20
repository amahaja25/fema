
<!-- rnb-text-begin -->

---
title: "R Notebook"
output: html_notebook
---

This is an [R Markdown](http://rmarkdown.rstudio.com) Notebook. When you execute code within the notebook, the results appear beneath the code. 

Try executing this chunk by clicking the *Run* button within the chunk or by placing your cursor inside it and pressing *Cmd+Shift+Enter*. 


<!-- rnb-text-end -->


<!-- rnb-chunk-begin -->


<!-- rnb-output-begin eyJkYXRhIjoiXG48IS0tIHJuYi1zb3VyY2UtYmVnaW4gZXlKa1lYUmhJam9pWUdCZ2NseHVhRzFoWDNCeWIycGxZM1J6SUNVK0pTQmNiaUFnWm1sc2RHVnlLSE4wWVhSbElEMDlJRndpVFdsamFHbG5ZVzVjSWlrZ0pUNGxJRnh1SUNCbWFXeDBaWElvY0hKdlozSmhiVVo1SUQwOUlESXdNakE2TWpBeU15a2dKVDRsSUZ4dUlDQm5jbTkxY0Y5aWVTaGpiM1Z1ZEhrcElDVStKU0JjYmlBZ2MzVnRiV0Z5YVhwbEtHTnZkVzUwUFc0b0tTa2dKVDRsSUZ4dUlDQmhjbkpoYm1kbEtHUmxjMk1vWTI5MWJuUXBLVnh1WEc1Z1lHQWlmUT09IC0tPlxuXG5gYGByXG5obWFfcHJvamVjdHMgJT4lIFxuICBmaWx0ZXIoc3RhdGUgPT0gXCJNaWNoaWdhblwiKSAlPiUgXG4gIGZpbHRlcihwcm9ncmFtRnkgPT0gMjAyMDoyMDIzKSAlPiUgXG4gIGdyb3VwX2J5KGNvdW50eSkgJT4lIFxuICBzdW1tYXJpemUoY291bnQ9bigpKSAlPiUgXG4gIGFycmFuZ2UoZGVzYyhjb3VudCkpXG5cbmBgYFxuXG48IS0tIHJuYi1zb3VyY2UtZW5kIC0tPlxuIn0= -->


<!-- rnb-source-begin eyJkYXRhIjoiYGBgclxuaG1hX3Byb2plY3RzICU+JSBcbiAgZmlsdGVyKHN0YXRlID09IFwiTWljaGlnYW5cIikgJT4lIFxuICBmaWx0ZXIocHJvZ3JhbUZ5ID09IDIwMjA6MjAyMykgJT4lIFxuICBncm91cF9ieShjb3VudHkpICU+JSBcbiAgc3VtbWFyaXplKGNvdW50PW4oKSkgJT4lIFxuICBhcnJhbmdlKGRlc2MoY291bnQpKVxuXG5gYGAifQ== -->

```r
hma_projects %>% 
  filter(state == "Michigan") %>% 
  filter(programFy == 2020:2023) %>% 
  group_by(county) %>% 
  summarize(count=n()) %>% 
  arrange(desc(count))

```

<!-- rnb-source-end -->


<!-- rnb-output-end -->

<!-- rnb-output-begin eyJkYXRhIjoiV2FybmluZzogVGhlcmUgd2FzIDEgd2FybmluZyBpbiBgZmlsdGVyKClgLlxu4oS5IEluIGFyZ3VtZW50OiBgcHJvZ3JhbUZ5ID09IDIwMjA6MjAyM2AuXG5DYXVzZWQgYnkgd2FybmluZyBpbiBgcHJvZ3JhbUZ5ID09IDIwMjA6MjAyM2A6XG4hIGxvbmdlciBvYmplY3QgbGVuZ3RoIGlzIG5vdCBhIG11bHRpcGxlIG9mIHNob3J0ZXIgb2JqZWN0IGxlbmd0aFxuIn0= -->

```
Warning: There was 1 warning in `filter()`.
ℹ In argument: `programFy == 2020:2023`.
Caused by warning in `programFy == 2020:2023`:
! longer object length is not a multiple of shorter object length
```



<!-- rnb-output-end -->

<!-- rnb-output-begin eyJkYXRhIjoiXG48IS0tIHJuYi1mcmFtZS1iZWdpbiBleUp0WlhSaFpHRjBZU0k2ZXlKamJHRnpjMlZ6SWpwYkluUmliRjlrWmlJc0luUmliQ0lzSW1SaGRHRXVabkpoYldVaVhTd2libkp2ZHlJNk1UQXNJbTVqYjJ3aU9qSXNJbk4xYlcxaGNua2lPbnNpUVNCMGFXSmliR1VpT2xzaU1UQWd3NWNnTWlKZGZYMHNJbkprWmlJNklrZzBjMGxCUVVGQlFVRkJRVUV6TVZKM1ZYSkVVVUpFWkhCR01VeEJhM0pDTnpKb1FXVjJSbUZGUlZaUlFrdDJXVFl6VTNwd2EzVXpkWGxZV2tkSWRucHhlakF5VkhWS1RYZFNkemhpVEV4MmVtSjVaRGt6WVdaaU1XSjZaRXBWUzBsVldtbElSV1JwU2toRmNqVlBka3czWlhoaFNVbE5aMFZ0VDFKa1VEbFFZa3h5UlZSVlpFOWpZVlpWYTBjNWQyTktja0UxUVcweVJteDZUMk5IUjNSTWMwRlNVRVoxVlRKdlNHazBjREpHZGtSR1kyeFFaU3RWY0RWQksyMUJLMnBEZFhFMFJTOWhVakZDSzNRcllqWmpiVTluWjJGeVUxQkViRnBDWjJrMlRXSnNSMk5PTnpkUmVFZzFhbVkxWm1ZMFNrdENlblJrVldOcFdYQjVkR1oxTTBSbmJHZzBUbVJGYm5CdE5Ia3hibGxJTkVONk9YUXlNelJRUW5scFRIaHRhMEZyTW10UFFXSk1NMFYyVjBscVoxQktlRThyUkRoUk5VWmpabU5GWTJsRFQzbG5SWGh5VmpOdVNrb3JjRlJsTWpKek5uTTFNMVZsV0ZZMVF6bHBSR3BsZURjNGVqUTFZazlyYUhoa2RUaExZMGhzYUdGWFIzUk1ORUZKYWprMGJYcG1WMjUzVVdsblMzTnNWVmRtUVVSMVV6VlhNM3BRVkdoNFVFVklhR3BFY25aSWIwTkJRVUU5SW4wPSAtLT5cblxuPGRpdiBkYXRhLXBhZ2VkdGFibGU9XCJmYWxzZVwiPlxuICA8c2NyaXB0IGRhdGEtcGFnZWR0YWJsZS1zb3VyY2UgdHlwZT1cImFwcGxpY2F0aW9uL2pzb25cIj5cbntcImNvbHVtbnNcIjpbe1wibGFiZWxcIjpbXCJjb3VudHlcIl0sXCJuYW1lXCI6WzFdLFwidHlwZVwiOltcImNoclwiXSxcImFsaWduXCI6W1wibGVmdFwiXX0se1wibGFiZWxcIjpbXCJjb3VudFwiXSxcIm5hbWVcIjpbMl0sXCJ0eXBlXCI6W1wiaW50XCJdLFwiYWxpZ25cIjpbXCJyaWdodFwiXX1dLFwiZGF0YVwiOlt7XCIxXCI6XCJXYXluZVwiLFwiMlwiOlwiNlwifSx7XCIxXCI6XCJPYWtsYW5kXCIsXCIyXCI6XCIyXCJ9LHtcIjFcIjpcIkFsbGVnYW5cIixcIjJcIjpcIjFcIn0se1wiMVwiOlwiQXJlbmFjXCIsXCIyXCI6XCIxXCJ9LHtcIjFcIjpcIkdsYWR3aW5cIixcIjJcIjpcIjFcIn0se1wiMVwiOlwiSW9zY29cIixcIjJcIjpcIjFcIn0se1wiMVwiOlwiTGl2aW5nc3RvblwiLFwiMlwiOlwiMVwifSx7XCIxXCI6XCJNYWNvbWJcIixcIjJcIjpcIjFcIn0se1wiMVwiOlwiU2hpYXdhc3NlZVwiLFwiMlwiOlwiMVwifSx7XCIxXCI6XCJTdGF0ZXdpZGVcIixcIjJcIjpcIjFcIn1dLFwib3B0aW9uc1wiOntcImNvbHVtbnNcIjp7XCJtaW5cIjp7fSxcIm1heFwiOlsxMF0sXCJ0b3RhbFwiOlsyXX0sXCJyb3dzXCI6e1wibWluXCI6WzEwXSxcIm1heFwiOlsxMF0sXCJ0b3RhbFwiOlsxMF19LFwicGFnZXNcIjp7fX19XG4gIDxcL3NjcmlwdD5cbjxcL2Rpdj5cblxuPCEtLSBybmItZnJhbWUtZW5kIC0tPlxuIn0= -->


<!-- rnb-frame-begin eyJtZXRhZGF0YSI6eyJjbGFzc2VzIjpbInRibF9kZiIsInRibCIsImRhdGEuZnJhbWUiXSwibnJvdyI6MTAsIm5jb2wiOjIsInN1bW1hcnkiOnsiQSB0aWJibGUiOlsiMTAgw5cgMiJdfX0sInJkZiI6Ikg0c0lBQUFBQUFBQUEzMVJ3VXJEUUJEZHBGMUxBa3JCNzJoQWV2RmFFRVZRQkt2WTYzU3pwa3UzdXlYWkdIdnpxejAyVHVKTXdSdzhiTEx2emJ5ZDkzYWZiMWJ6ZEpVS0lVWmlIRWRpSkhFcjVPdkw3ZXhhSUlNZ0VtT1JkUDlQYkxyRVRVZE9jYVZVa0c5d2NKckE1QW0yRmx6T2NHR3RMc0FSUEZ1VTJvSGk0cDJGdkRGY2xQZStVcDVBK21BK2pDdXE0RS9hUjFCK3QrYjZjbU9nZ2FyU1BEbFpCZ2k2TWJsR2NONzdReEg1amY1ZmY0SktCenRkVWNpWXB5dGZ1M0RnbGg0TmRFbnBtNHkxbllINEN6OXQyMzRQQnlpTHhta0FrMmtPQWJMM0V2V0lqZ1BKeE8rRDhRNUZjZmNFY2lDT3lnRXhyVjNuSkorcFRlMjJzNnM1M1VlWFY1QzlpRGpleDc4ejQ1Yk9raHhkdThLY0hsaGFXR3RMNEFJajk0bXpmV253UWlnS3NsVVdmQUR1UzVXM3pQVGh4UEVIaGpEcnZIb0NBQUE9In0= -->

<div data-pagedtable="false">
  <script data-pagedtable-source type="application/json">
{"columns":[{"label":["county"],"name":[1],"type":["chr"],"align":["left"]},{"label":["count"],"name":[2],"type":["int"],"align":["right"]}],"data":[{"1":"Wayne","2":"6"},{"1":"Oakland","2":"2"},{"1":"Allegan","2":"1"},{"1":"Arenac","2":"1"},{"1":"Gladwin","2":"1"},{"1":"Iosco","2":"1"},{"1":"Livingston","2":"1"},{"1":"Macomb","2":"1"},{"1":"Shiawassee","2":"1"},{"1":"Statewide","2":"1"}],"options":{"columns":{"min":{},"max":[10],"total":[2]},"rows":{"min":[10],"max":[10],"total":[10]},"pages":{}}}
  </script>
</div>

<!-- rnb-frame-end -->


<!-- rnb-output-end -->

<!-- rnb-chunk-end -->


<!-- rnb-text-begin -->


Add a new chunk by clicking the *Insert Chunk* button on the toolbar or by pressing *Cmd+Option+I*.

When you save the notebook, an HTML file containing the code and output will be saved alongside it (click the *Preview* button or press *Cmd+Shift+K* to preview the HTML file). 

The preview shows you a rendered HTML copy of the contents of the editor. Consequently, unlike *Knit*, *Preview* does not run any R code chunks. Instead, the output of the chunk when it was last run in the editor is displayed.


<!-- rnb-text-end -->

