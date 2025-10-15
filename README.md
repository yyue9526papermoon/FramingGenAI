# News Topic Classification (Hugging Face)

## Models tested
- `nabeelshan/distilbert-finetuned-agnews`  
  - `id2label`: {0: World, 1: Sports, 2: Business, 3: Sci/Tech}  
  - **Examples**
    - Senate bill headline → **World** (0.928)
    - Apple chip headline → **Sci/Tech** (0.912)
    - Real Madrid headline → **World** (0.881)

- `textattack/bert-base-uncased-ag-news`  
  - Original labels are `LABEL_0..3`; we map them to {World, Sports, Business, Sci/Tech}.  
  - **Examples**
    - Senate bill headline → **World** (0.999)
    - Apple chip headline → **Sci/Tech** (0.933)
    - Real Madrid headline → **World** (0.998)

## Takeaway
Both AG-News–fine-tuned models work out of the box for topic labeling.  
`nabeelshan/...` provides readable labels; `textattack/...` needs a label mapping but shows consistent scores.
