# H&M personalized Fashion recommendation

## Problem statement
H&M Group is a family of brands and businesses with 53 online markets and approximately 4,850 stores. Online store offers shoppers an extensive selection of products to browse through. But with too many choices, customers might not quickly find what interests them or what they are looking for, and ultimately, they might not make a purchase. 

Advantages: 
- More conversions
- Enhance the shopping experience by directly suggesting the right product.
- More importantly, helping customers make the right choices also has a positive implications for sustainability, as it **reduces returns**, and thereby minimizes emissions from transportation.

## Comp details 

In this competition, H&M Group invites you to develop product recommendations based on data from previous transactions, as well as from customer and product meta data. The available meta data spans from simple data, such as garment type and customer age, to text data from product descriptions, to image data from garment images.


## Metrics
Mean Average Precision @ 12 (MAP@12):

𝑀𝐴𝑃@12=1𝑈∑𝑢=1𝑈∑𝑘=1𝑚𝑖𝑛(𝑛,12)𝑃(𝑘)×𝑟𝑒𝑙(𝑘)

where 𝑈 is the number of customers, 𝑃(𝑘) is the precision at cutoff 𝑘, 𝑛 is the number predictions per customer, and 𝑟𝑒𝑙(𝑘) is an indicator function equaling 1 if the item at rank 𝑘 is a relevant (correct) label, zero otherwise.

- You will be making purchase predictions for all customer_id values provided, regardless of whether these customers made purchases in the training data.
- Customer that did not make any purchase during test period are excluded from the scoring.
- There is never a penalty for using the full 12 predictions for a customer that ordered fewer than 12 items; thus, it's advantageous to make 12 predictions for each customer.

## Data

```
kaggle competitions download -p input/ -c h-and-m-personalized-fashion-recommendations
```
## Dependencies

```python
conda env create -f <your-env-name>
conda activate <your-env-name> # eg: hm-rec
pip install -r requirements.txt

# if you want to select notebook the same environment as kernel
# Simply start jupyter notebook after activating the env
conda activate <your-env-name>
jupyter notebook

# alternate
conda install -c anaconda ipykernel ipython_genutils
ipython kernel install --user --name=<your-env-name>
```

## References
[Kaggle notebooks, discussions and helpful links](notebooks/references.txt)