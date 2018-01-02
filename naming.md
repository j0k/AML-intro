# Cross Naming and Identification System (CNIS)

That part of AML is one of the most challenged part course is intensive use of ML algorithms
and deep connection with AML IDE. I see in CNIS lot of capabilities to be simple.

Examples:
Json/dict object:
```
dic = {}
dic['ex0'] = 'Cat'
dic['ex1'] = 'Dog'
dic['ex0_min_price'] = 120
dic['ex0_max_price'] = 660
dic['ex1_min_price'] = 120
dic['ex1_max_price'] = 460

dic['ex0_avg_price'] = 320
dic['ex1_avg_price'] = 300
```

or the same physic object can have another form like:
```
dic = {}
dic['ex0'] = {}
dic['ex1'] = {}

dic['ex0']['title'] = 'Cat'
dic['ex1']['title'] = 'Dog'

dic['ex0']['price'] = {}
dic['ex1']['price'] = {}

dic['ex0']['price']['min'] = 120
dic['ex0']['price']['max'] = 660
dic['ex0']['price']['avg'] = 320

dic['ex1']['price']['min'] = 120
dic['ex1']['price']['max'] = 460
dic['ex1']['price']['avg'] = 300
```

and now I would like to print a text which will report data details like next:
```
TEXT = """
Today we have two lot types: {ex0} and {ex1}.

Minimal price of {ex0} is {e0_pmin}, maximum is {e0_pmax} and average is {e0_pavg}.
Minimal price of {ex1} is {e1_pmin}, maximum is {e1_pmax} and average is {e1_pavg}.
"""

TEXT.format(ex0 = dic['ex0'],
            ex1 = dic['ex1'],
            e0_pmin = dic['ex0_min_price'],
            e0_pmax = dic['ex0_max_price'],
            e0_pavg = dic['ex0_avg_price'],
            e1_pmin = dic['ex1_min_price'],
            e1_pmax = dic['ex1_max_price'],
            e1_pavg = dic['ex1_avg_price'])
```

For the first example.

It will be more useful to write that code in the combined mode:
* visual-choosing
* substitute
* text navigation
* auto-code generation

The vision is next. In visual mode you can substitute dic['ex0'] at {ex0} and ask
to generate other substitutions. Also you can push the **dic** object and drag-n-drop
sample of fields to {} vars in **TEXT**. AML IDE will save the result and also your
  operations to repeat them in future if smth change.
