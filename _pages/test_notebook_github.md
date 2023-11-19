---
permalink: /jupyter/
title: "Jupyter To Markdown"
author_profile: true
redirect_from: 
  - /jupyter.html
---

```python
import datetime
import logging
import os
import requests
import pandas as pd
import numpy as np
import time
```


```python
SquareAccessToken = ''

```


```python
# headers = {
#     'Square-Version': '2023-08-16',
#     'Authorization': 'Bearer ' + SquareAccessToken,
#     'Content-Type': 'application/json',
# }

# json_data = {
#     'query': {
#         'filter': {
#             'date_time_filter': {
#                 'created_at': {
#                     'start_at': '2022-01-01',
#                     'end_at': '2023-08-31',
#                 },
#             },
#         },
#     },
#     'location_ids': [
#         'LKTC8N219STHK',
#         'L7A3N80532N0J',
#         'L8J7XNE0KQFR0',
#         'LGSF3NJ8JMK87',
#         'LPMDYWPHRFPW1',
#         'LG4TF88099YNE',
#         'L1FQP1GE5WVW2',
#     ],
# }


# locations_url = 'https://connect.squareup.com/v2/locations'
# response = requests.get(locations_url, headers=headers)
# print(response.status_code)
# print(response.json())
```


```python

# headers = {
#     'Square-Version': '2023-08-16',
#     'Authorization': 'Bearer ' + SquareAccessToken,
#     'Content-Type': 'application/json',
# }

# json_data = {
#     'query': {
#         'filter': {
#             'date_time_filter': {
#                 'created_at': {
#                     'start_at': '2022-01-01',
#                     'end_at': '2023-08-31',
#                 },
#             },
#         },
#     },
#     'location_ids': [
#         'LKTC8N219STHK',
#         'L7A3N80532N0J',
#         'L8J7XNE0KQFR0',
#         'LGSF3NJ8JMK87',
#         'LPMDYWPHRFPW1',
#         'LG4TF88099YNE',
#         'L1FQP1GE5WVW2',
#     ],
# }

# ordersearch_url = 'https://connect.squareup.com/v2/orders/search'

# # response = requests.post(ordersearch_url, headers=headers, json=json_data)

# # if response.status_code == 200:
# #     orders = response.json()['orders']
# # df = pd.json_normalize(orders)
# response = requests.post(ordersearch_url, headers=headers, json=json_data)
# print(response.status_code)
# # print(response.json())
# orders = response.json()['orders']
# i = 0
# while 'cursor' in response.json():
#     json_data['cursor'] = response.json()['cursor']
#     response = requests.post(ordersearch_url, headers=headers, json=json_data)
#     orders.extend(response.json()['orders'])
#     # i = i + 1
#     # print(i)
#     time.sleep(3)

# df = pd.json_normalize(orders)

```


```python
# def extract_json(df, target_col, id_col, tid_name):
#     filtered_df = df[df[target_col].notna()][[target_col, id_col]]
#     explode_df = filtered_df.explode(target_col).reset_index(drop=True)
#     explode_df = explode_df.rename(columns={id_col: tid_name})
#     final_df = pd.json_normalize(explode_df[target_col])
#     # lineItem_df = lineItem_df.rename(columns={'id': 'refund_id'})
#     final_df[tid_name] = explode_df[tid_name].values

#     cols = final_df.columns.tolist()
#     cols = [cols[-1]] + cols[:-1]
#     final_df = final_df[cols]
#     # final_df.columns = final_df.columns.str.replace('.', '_')
    
#     return final_df

# def get_applied_amount(lineitem_df):
#     try:
#         applied_taxes_df = extract_json(lineitem_df, 'applied_taxes', 'uid', 'lineitem_id')    
#     except:
#         applied_taxes_df = pd.DataFrame(columns=['lineitem_id', 'uid', 'tax_uid', 'applied_money.amount', 'applied_money.currency'])
#         # applied_taxes_df.columns = applied_taxes_df.columns.str.replace('.', '_')
        
#     try:
#         applied_discounts_df = extract_json(lineitem_df, 'applied_discounts', 'uid', 'lineitem_id')    
#     except:
#         applied_discounts_df = pd.DataFrame(columns=['lineitem_id', 'uid', 'discount_uid', 'applied_money.amount', 'applied_money.currency'])
#         # applied_discounts_df.columns = applied_discounts_df.columns.str.replace('.', '_')
        
#     try:
#         applied_service_charges_df = extract_json(lineitem_df, 'applied_service_charges', 'uid', 'lineitem_id')
#     except:
#         applied_service_charges_df = pd.DataFrame(columns=['lineitem_id', 'uid', 'service_charge_uid', 'applied_money.amount', 'applied_money.currency'])
#         # applied_service_charges_df.columns = applied_service_charges_df.columns.str.replace('.', '_')
        
#     return applied_taxes_df, applied_discounts_df, applied_service_charges_df

```


```python
# def process_and_save_df(df):
#     try:
#         refund_df = extract_json(df, 'refunds', 'id', 'order_id')
#         refund_df = refund_df.rename(columns={'id': 'refund_id'})
        
#     except:
#         refund_df = pd.DataFrame(columns=['order_id', 'refund_id', 'location_id', 'transaction_id', 'tender_id',
#         'created_at', 'reason', 'status', 'amount_money.amount',
#         'amount_money.currency', 'processing_fee_money.amount',
#         'processing_fee_money.currency'])
#         # refund_df.columns = refund_df.columns.str.replace('.', '_')

#     try:
#         lineItem_df = extract_json(df, 'line_items', 'id', 'order_id')
        
#     except:
#         lineItem_df = pd.DataFrame(columns=['order_id', 'uid', 'catalog_object_id', 'catalog_version', 'quantity',
#         'name', 'variation_name', 'item_type', 'base_price_money.amount',
#         'base_price_money.currency', 'gross_sales_money.amount',
#         'gross_sales_money.currency', 'total_tax_money.amount',
#         'total_tax_money.currency', 'total_discount_money.amount',
#         'total_discount_money.currency', 'total_money.amount',
#         'total_money.currency', 'variation_total_price_money.amount',
#         'variation_total_price_money.currency',
#         'total_service_charge_money.amount',
#         'total_service_charge_money.currency', 'applied_taxes', 'note',
#         'applied_discounts', 'modifiers'])
#         # lineItem_df.columns = lineItem_df.columns.str.replace('.', '_')

#     try:
#         return_df = extract_json(df, 'returns', 'id', 'order_id')
#     except:
#         return_df = pd.DataFrame(columns=['order_id', 'source_order_id', 'return_line_items', 'return_service_charges', 'return_taxes', 'uid'])
#         # return_df.columns = lineItem_df.columns.str.replace('.', '_')

    
#     try:
#         return_line_items_df = extract_json(return_df, 'return_line_items', 'source_order_id', 'source_order_id')
#     except:
#         return_line_items_df = pd.DataFrame(columns=['source_order_id', 'uid', 'source_line_item_uid', 'name', 'quantity',
#         'catalog_object_id', 'catalog_version', 'variation_name', 'item_type',
#         'base_price_money.amount', 'base_price_money.currency',
#         'variation_total_price_money.amount',
#         'variation_total_price_money.currency', 'gross_return_money.amount',
#         'gross_return_money.currency', 'total_tax_money.amount',
#         'total_tax_money.currency', 'total_discount_money.amount',
#         'total_discount_money.currency', 'total_money.amount',
#         'total_money.currency', 'total_service_charge_money.amount',
#         'total_service_charge_money.currency', 'applied_taxes'])
#         # return_line_items_df.columns = lineItem_df.columns.str.replace('.', '_')

#     applied_taxes_df, applied_discounts_df, applied_service_charges_df = get_applied_amount(lineItem_df)
#     ri_applied_taxes_df, ri_applied_discounts_df, ri_applied_service_charges_df = get_applied_amount(return_line_items_df)

#     final_applied_taxes_df = pd.concat([applied_taxes_df, ri_applied_taxes_df], ignore_index=True)
#     final_applied_discounts_df = pd.concat([applied_discounts_df, ri_applied_discounts_df], ignore_index=True)
#     final_applied_service_charges_df = pd.concat([applied_service_charges_df, ri_applied_service_charges_df], ignore_index=True)

#     final_return_df = return_df.drop(['return_line_items', 'return_service_charges', 'return_taxes', 'return_discounts'], axis=1, errors='ignore')
#     final_lineItem_df = lineItem_df.drop(['applied_taxes', 'applied_discounts', 'modifiers', 'applied_service_charges', 'returned_quantities', 'pricing_blocklists.blocked_discounts', 'pricing_blocklists.blocked_taxes'], axis=1, errors='ignore')
#     final_return_line_items_df = return_line_items_df.drop(['applied_taxes', 'applied_discounts', 'applied_service_charges'], axis=1, errors='ignore')
#     final_refund_df = refund_df

#     desired_columns = ['id', 'location_id', 'source_name', 'customer_id', 'created_at', 'updated_at', 'state', 'version', 
#                     'rounding_adjustment.uid', 'rounding_adjustment.name', 'rounding_adjustment.amount_money.amount', 'rounding_adjustment.amount_money.amount_money.currency', 
#                     'total_tip_money.amount', 'total_tip_money.currency']
#     for col in desired_columns:
#         if col not in df.columns:
#             df[col] = np.nan
            
#     final_order_df = df[desired_columns]
#     # final_order_df['created_at'] = pd.to_datetime(final_order_df['created_at']).dt.strftime('%Y-%m-%dT%H:%M:%SZ')
#     # final_order_df['updated_at'] = pd.to_datetime(final_order_df['updated_at']).dt.strftime('%Y-%m-%dT%H:%M:%SZ')
#     # final_order_df.columns = final_order_df.columns.str.replace('.', '_')


#     applied_taxes_BlobName= "parquets/LineItemAppliedTaxes.parquet"
#     applied_discounts_BlobName= "parquets/LineItemAppliedDiscounts.parquet"
#     applied_service_charges_BlobName= "parquets/LineItemAppliedServiceCharges.parquet"
#     return_BlobName= "parquets/Returns.parquet"
#     lineItem_BlobName= "parquets/LineItem.parquet"
#     return_line_items_BlobName= "parquets/ReturnLineItem.parquet"
#     refund_BlobName= "parquets/Refund.parquet"
#     order_BlobName= "parquets/Orders.parquet"


#     logging.info("Creating parquet file in local /tmp/ directory")
#     final_applied_taxes_df.to_parquet(applied_taxes_BlobName, index=False)
#     final_applied_discounts_df.to_parquet(applied_discounts_BlobName, index=False)
#     final_applied_service_charges_df.to_parquet(applied_service_charges_BlobName, index=False)
#     final_return_df.to_parquet(return_BlobName, index=False)
#     final_lineItem_df.to_parquet(lineItem_BlobName, index=False)
#     final_return_line_items_df.to_parquet(return_line_items_BlobName, index=False)
#     final_refund_df.to_parquet(refund_BlobName, index=False)
#     final_order_df.to_parquet(order_BlobName, index=False)
```


```python
# process_and_save_df(df)
```


```python

```


```python
df_orders = pd.read_parquet('parquets_historical/Orders.parquet')
df_lineItem = pd.read_parquet('parquets_historical/LineItem.parquet')
df_lineItemAppliedDiscounts = pd.read_parquet('parquets_historical/LineItemAppliedDiscounts.parquet')
df_lineItemAppliedServiceCharges = pd.read_parquet('parquets_historical/LineItemAppliedServiceCharges.parquet')
df_lineItemAppliedTaxes = pd.read_parquet('parquets_historical/LineItemAppliedTaxes.parquet')
df_refund = pd.read_parquet('parquets_historical/Refund.parquet')
df_returnLineItem = pd.read_parquet('parquets_historical/ReturnLineItem.parquet')
df_returns = pd.read_parquet('parquets_historical/Returns.parquet')
```


```python
df_lineItem_september = pd.read_parquet('parquets_since_september/LineItem.parquet')
df_returnLineItem_september = pd.read_parquet('parquets_since_september/ReturnLineItem.parquet')
df_returns_september = pd.read_parquet('parquets_since_september/Returns.parquet')
```

#### LIST OF COLUMNS


```python
df_orders.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 149964 entries, 0 to 149963
    Data columns (total 14 columns):
     #   Column                                                  Non-Null Count   Dtype  
    ---  ------                                                  --------------   -----  
     0   id                                                      149964 non-null  object 
     1   location_id                                             149964 non-null  object 
     2   source_name                                             0 non-null       float64
     3   customer_id                                             7925 non-null    object 
     4   created_at                                              149964 non-null  object 
     5   updated_at                                              149964 non-null  object 
     6   state                                                   149964 non-null  object 
     7   version                                                 13765 non-null   float64
     8   rounding_adjustment.uid                                 0 non-null       float64
     9   rounding_adjustment.name                                0 non-null       float64
     10  rounding_adjustment.amount_money.amount                 0 non-null       float64
     11  rounding_adjustment.amount_money.amount_money.currency  0 non-null       float64
     12  total_tip_money.amount                                  149767 non-null  float64
     13  total_tip_money.currency                                149767 non-null  object 
    dtypes: float64(7), object(7)
    memory usage: 16.0+ MB



```python
df_lineItem.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 220257 entries, 0 to 220256
    Data columns (total 24 columns):
     #   Column                                Non-Null Count   Dtype  
    ---  ------                                --------------   -----  
     0   order_id                              220257 non-null  object 
     1   uid                                   220257 non-null  object 
     2   catalog_object_id                     217461 non-null  object 
     3   catalog_version                       217461 non-null  float64
     4   quantity                              220257 non-null  object 
     5   name                                  218927 non-null  object 
     6   variation_name                        217461 non-null  object 
     7   item_type                             220257 non-null  object 
     8   base_price_money.amount               220257 non-null  int64  
     9   base_price_money.currency             220257 non-null  object 
     10  gross_sales_money.amount              220257 non-null  int64  
     11  gross_sales_money.currency            220257 non-null  object 
     12  total_tax_money.amount                220257 non-null  int64  
     13  total_tax_money.currency              220257 non-null  object 
     14  total_discount_money.amount           220257 non-null  int64  
     15  total_discount_money.currency         220257 non-null  object 
     16  total_money.amount                    220257 non-null  int64  
     17  total_money.currency                  220257 non-null  object 
     18  variation_total_price_money.amount    220257 non-null  int64  
     19  variation_total_price_money.currency  220257 non-null  object 
     20  total_service_charge_money.amount     220256 non-null  float64
     21  total_service_charge_money.currency   220256 non-null  object 
     22  note                                  1808 non-null    object 
     23  tare_quantity                         2 non-null       object 
    dtypes: float64(2), int64(6), object(16)
    memory usage: 40.3+ MB



```python
df_lineItemAppliedDiscounts.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 8503 entries, 0 to 8502
    Data columns (total 5 columns):
     #   Column                  Non-Null Count  Dtype 
    ---  ------                  --------------  ----- 
     0   lineitem_id             8503 non-null   object
     1   uid                     8503 non-null   object
     2   discount_uid            8503 non-null   object
     3   applied_money.amount    8503 non-null   int64 
     4   applied_money.currency  8503 non-null   object
    dtypes: int64(1), object(4)
    memory usage: 332.3+ KB



```python
df_lineItemAppliedServiceCharges.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 0 entries
    Data columns (total 5 columns):
     #   Column                  Non-Null Count  Dtype 
    ---  ------                  --------------  ----- 
     0   lineitem_id             0 non-null      object
     1   uid                     0 non-null      object
     2   service_charge_uid      0 non-null      object
     3   applied_money.amount    0 non-null      object
     4   applied_money.currency  0 non-null      object
    dtypes: object(5)
    memory usage: 132.0+ bytes



```python
df_lineItemAppliedTaxes.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 197318 entries, 0 to 197317
    Data columns (total 5 columns):
     #   Column                  Non-Null Count   Dtype 
    ---  ------                  --------------   ----- 
     0   lineitem_id             197318 non-null  object
     1   uid                     197318 non-null  object
     2   tax_uid                 197318 non-null  object
     3   applied_money.amount    197318 non-null  int64 
     4   applied_money.currency  197318 non-null  object
    dtypes: int64(1), object(4)
    memory usage: 7.5+ MB



```python
df_refund.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 651 entries, 0 to 650
    Data columns (total 12 columns):
     #   Column                         Non-Null Count  Dtype  
    ---  ------                         --------------  -----  
     0   order_id                       651 non-null    object 
     1   refund_id                      651 non-null    object 
     2   location_id                    651 non-null    object 
     3   transaction_id                 651 non-null    object 
     4   tender_id                      651 non-null    object 
     5   created_at                     651 non-null    object 
     6   reason                         651 non-null    object 
     7   status                         651 non-null    object 
     8   amount_money.amount            651 non-null    int64  
     9   amount_money.currency          651 non-null    object 
     10  processing_fee_money.amount    454 non-null    float64
     11  processing_fee_money.currency  454 non-null    object 
    dtypes: float64(1), int64(1), object(10)
    memory usage: 61.2+ KB



```python
df_returnLineItem.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 984 entries, 0 to 983
    Data columns (total 25 columns):
     #   Column                                Non-Null Count  Dtype  
    ---  ------                                --------------  -----  
     0   source_order_id                       984 non-null    object 
     1   uid                                   984 non-null    object 
     2   source_line_item_uid                  736 non-null    object 
     3   name                                  713 non-null    object 
     4   quantity                              984 non-null    object 
     5   catalog_object_id                     712 non-null    object 
     6   catalog_version                       712 non-null    float64
     7   variation_name                        712 non-null    object 
     8   item_type                             984 non-null    object 
     9   base_price_money.amount               984 non-null    int64  
     10  base_price_money.currency             984 non-null    object 
     11  variation_total_price_money.amount    984 non-null    int64  
     12  variation_total_price_money.currency  984 non-null    object 
     13  gross_return_money.amount             984 non-null    int64  
     14  gross_return_money.currency           984 non-null    object 
     15  total_tax_money.amount                984 non-null    int64  
     16  total_tax_money.currency              984 non-null    object 
     17  total_discount_money.amount           984 non-null    int64  
     18  total_discount_money.currency         984 non-null    object 
     19  total_money.amount                    984 non-null    int64  
     20  total_money.currency                  984 non-null    object 
     21  total_service_charge_money.amount     827 non-null    float64
     22  total_service_charge_money.currency   827 non-null    object 
     23  note                                  9 non-null      object 
     24  return_modifiers                      4 non-null      object 
    dtypes: float64(2), int64(6), object(17)
    memory usage: 192.3+ KB



```python
df_returns.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 921 entries, 0 to 920
    Data columns (total 4 columns):
     #   Column           Non-Null Count  Dtype 
    ---  ------           --------------  ----- 
     0   order_id         921 non-null    object
     1   source_order_id  921 non-null    object
     2   uid              197 non-null    object
     3   return_tips      25 non-null     object
    dtypes: object(4)
    memory usage: 28.9+ KB


#### TROUBLESHOOTING DF_RETURNLINEITEM FOR WAREHOUSE INGESTION


```python
df_returnLineItem_september.columns
```




    Index(['source_order_id', 'uid', 'quantity', 'item_type',
           'base_price_money.amount', 'base_price_money.currency',
           'variation_total_price_money.amount',
           'variation_total_price_money.currency', 'gross_return_money.amount',
           'gross_return_money.currency', 'total_tax_money.amount',
           'total_tax_money.currency', 'total_discount_money.amount',
           'total_discount_money.currency', 'total_money.amount',
           'total_money.currency', 'total_service_charge_money.amount',
           'total_service_charge_money.currency', 'source_line_item_uid', 'name',
           'catalog_object_id', 'catalog_version', 'variation_name', 'note'],
          dtype='object')




```python
df_returnLineItem.columns
```




    Index(['source_order_id', 'uid', 'source_line_item_uid', 'name', 'quantity',
           'catalog_object_id', 'catalog_version', 'variation_name', 'item_type',
           'base_price_money.amount', 'base_price_money.currency',
           'variation_total_price_money.amount',
           'variation_total_price_money.currency', 'gross_return_money.amount',
           'gross_return_money.currency', 'total_tax_money.amount',
           'total_tax_money.currency', 'total_discount_money.amount',
           'total_discount_money.currency', 'total_money.amount',
           'total_money.currency', 'total_service_charge_money.amount',
           'total_service_charge_money.currency', 'note', 'return_modifiers'],
          dtype='object')




```python
df_returnLineItem.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 984 entries, 0 to 983
    Data columns (total 25 columns):
     #   Column                                Non-Null Count  Dtype  
    ---  ------                                --------------  -----  
     0   source_order_id                       984 non-null    object 
     1   uid                                   984 non-null    object 
     2   source_line_item_uid                  736 non-null    object 
     3   name                                  713 non-null    object 
     4   quantity                              984 non-null    object 
     5   catalog_object_id                     712 non-null    object 
     6   catalog_version                       712 non-null    float64
     7   variation_name                        712 non-null    object 
     8   item_type                             984 non-null    object 
     9   base_price_money.amount               984 non-null    int64  
     10  base_price_money.currency             984 non-null    object 
     11  variation_total_price_money.amount    984 non-null    int64  
     12  variation_total_price_money.currency  984 non-null    object 
     13  gross_return_money.amount             984 non-null    int64  
     14  gross_return_money.currency           984 non-null    object 
     15  total_tax_money.amount                984 non-null    int64  
     16  total_tax_money.currency              984 non-null    object 
     17  total_discount_money.amount           984 non-null    int64  
     18  total_discount_money.currency         984 non-null    object 
     19  total_money.amount                    984 non-null    int64  
     20  total_money.currency                  984 non-null    object 
     21  total_service_charge_money.amount     827 non-null    float64
     22  total_service_charge_money.currency   827 non-null    object 
     23  note                                  9 non-null      object 
     24  return_modifiers                      4 non-null      object 
    dtypes: float64(2), int64(6), object(17)
    memory usage: 192.3+ KB



```python
df_returnLineItem[~df_returnLineItem['return_modifiers'].isnull()] # ['return_modifiers']
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>source_order_id</th>
      <th>uid</th>
      <th>source_line_item_uid</th>
      <th>name</th>
      <th>quantity</th>
      <th>catalog_object_id</th>
      <th>catalog_version</th>
      <th>variation_name</th>
      <th>item_type</th>
      <th>base_price_money.amount</th>
      <th>...</th>
      <th>total_tax_money.amount</th>
      <th>total_tax_money.currency</th>
      <th>total_discount_money.amount</th>
      <th>total_discount_money.currency</th>
      <th>total_money.amount</th>
      <th>total_money.currency</th>
      <th>total_service_charge_money.amount</th>
      <th>total_service_charge_money.currency</th>
      <th>note</th>
      <th>return_modifiers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>797</th>
      <td>PPeAyE5qB3yNgZ2hh9mDa4geV</td>
      <td>20A694F6-71B4-4463-AC5E-E6015AC7864B</td>
      <td>69304d18-ce28-4e9c-b477-0f1d0e6e0e7f</td>
      <td>Import/Craft</td>
      <td>1</td>
      <td>CV4SQG66XGGDAXBXERGPN6HL</td>
      <td>1.674169e+12</td>
      <td>Regular</td>
      <td>ITEM</td>
      <td>1100</td>
      <td>...</td>
      <td>89</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
      <td>1189</td>
      <td>USD</td>
      <td>0.0</td>
      <td>USD</td>
      <td>None</td>
      <td>[{'base_price_money': {'amount': 0, 'currency'...</td>
    </tr>
    <tr>
      <th>802</th>
      <td>Pj0KSViaAU381r6g4xvagC5eV</td>
      <td>F2BBCEDE-0DA1-4CD7-8DCC-FF8FEE689B3D</td>
      <td>66b8608e-62af-4fcb-b111-9cfe34023e38</td>
      <td>Import/Craft</td>
      <td>1</td>
      <td>CV4SQG66XGGDAXBXERGPN6HL</td>
      <td>1.674169e+12</td>
      <td>Regular</td>
      <td>ITEM</td>
      <td>1100</td>
      <td>...</td>
      <td>89</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
      <td>1189</td>
      <td>USD</td>
      <td>0.0</td>
      <td>USD</td>
      <td>None</td>
      <td>[{'base_price_money': {'amount': 0, 'currency'...</td>
    </tr>
    <tr>
      <th>807</th>
      <td>nnmxCIxCpM1UMmvQNAHKc8meV</td>
      <td>C04B9045-76EA-4E43-855D-E6DF5997435D</td>
      <td>01704f20-4469-4fd4-9c98-3c27d47c62e8</td>
      <td>Mixed</td>
      <td>1</td>
      <td>VLTPM346IWRD2RVZ4YA7FOY3</td>
      <td>1.674173e+12</td>
      <td>Regular</td>
      <td>ITEM</td>
      <td>1200</td>
      <td>...</td>
      <td>97</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
      <td>1297</td>
      <td>USD</td>
      <td>0.0</td>
      <td>USD</td>
      <td>None</td>
      <td>[{'base_price_money': {'amount': 0, 'currency'...</td>
    </tr>
    <tr>
      <th>808</th>
      <td>VMX0FIU2hG6uOV3pldBl9ZweV</td>
      <td>BAB887C3-DD78-4D3B-9512-BF815BD6CB1A</td>
      <td>17a50b80-9725-4b1e-aee8-eced1ac984ce</td>
      <td>Import/Craft</td>
      <td>1</td>
      <td>CV4SQG66XGGDAXBXERGPN6HL</td>
      <td>1.674170e+12</td>
      <td>Regular</td>
      <td>ITEM</td>
      <td>1100</td>
      <td>...</td>
      <td>89</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
      <td>1189</td>
      <td>USD</td>
      <td>0.0</td>
      <td>USD</td>
      <td>None</td>
      <td>[{'base_price_money': {'amount': 0, 'currency'...</td>
    </tr>
  </tbody>
</table>
<p>4 rows × 25 columns</p>
</div>




```python
df_returnLineItem[~df_returnLineItem['return_modifiers'].isnull()]['return_modifiers'].to_json('nhat_meeting_Nov,01,2023/returnLineItem[return_modifiers].json')
```


```python

```


```python

```


```python
df_test = extract_json(df_returnLineItem, 'return_modifiers', 'uid', 'returnLineItemIdentifier')
```


```python
df_test
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>returnLineItemIdentifier</th>
      <th>catalog_object_id</th>
      <th>catalog_version</th>
      <th>name</th>
      <th>uid</th>
      <th>base_price_money.amount</th>
      <th>base_price_money.currency</th>
      <th>total_price_money.amount</th>
      <th>total_price_money.currency</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20A694F6-71B4-4463-AC5E-E6015AC7864B</td>
      <td>I36V46ARJRJ4CC3IPB5ADITZ</td>
      <td>1674168387533</td>
      <td>Blue Moon</td>
      <td>c59ebcdd-b924-4f74-b9a9-cb652b351916</td>
      <td>0</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
    </tr>
    <tr>
      <th>1</th>
      <td>F2BBCEDE-0DA1-4CD7-8DCC-FF8FEE689B3D</td>
      <td>XSWWWDOWUX7AIOQHMEE2D7AR</td>
      <td>1674169419140</td>
      <td>Hop Valley Panda Stash</td>
      <td>f0cd4652-a66e-452f-810d-10e9905fefb7</td>
      <td>0</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
    </tr>
    <tr>
      <th>2</th>
      <td>C04B9045-76EA-4E43-855D-E6DF5997435D</td>
      <td>U7YIVPX7V26VKPTBVCPWJWLW</td>
      <td>1674168267987</td>
      <td>Vodka</td>
      <td>38dab45d-c09a-47b3-9019-fd70253cc487</td>
      <td>0</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BAB887C3-DD78-4D3B-9512-BF815BD6CB1A</td>
      <td>JB362KTOFX4DL3ZJWHFGDPLY</td>
      <td>1674169419140</td>
      <td>Vizzy Strawberry Orange</td>
      <td>c5d3a21b-ac1b-4418-bb86-8dd272d01531</td>
      <td>0</td>
      <td>USD</td>
      <td>0</td>
      <td>USD</td>
    </tr>
  </tbody>
</table>
</div>



#### TROUBLESHOOTING DF_RETURNs FOR WAREHOUSE INGESTION


```python
df_returns_september.columns
```




    Index(['order_id', 'source_order_id', 'uid'], dtype='object')




```python
df_returns.columns
```




    Index(['order_id', 'source_order_id', 'uid', 'return_tips'], dtype='object')




```python
df_returns.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 921 entries, 0 to 920
    Data columns (total 4 columns):
     #   Column           Non-Null Count  Dtype 
    ---  ------           --------------  ----- 
     0   order_id         921 non-null    object
     1   source_order_id  921 non-null    object
     2   uid              197 non-null    object
     3   return_tips      25 non-null     object
    dtypes: object(4)
    memory usage: 28.9+ KB



```python
df_returns[df_returns['return_tips'].notnull()] # ['return_tips']
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>order_id</th>
      <th>source_order_id</th>
      <th>uid</th>
      <th>return_tips</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>63</th>
      <td>Ni0CAwedQnzdY54qVoA6wKveV</td>
      <td>TrXQ3CCoJEqHYn98gDW43u2eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 1920, 'currency'...</td>
    </tr>
    <tr>
      <th>161</th>
      <td>jZ6oDISxNCRULDmo1kDA1p8eV</td>
      <td>pe3iTB9di94NMRPUAjZhog5eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 660, 'currency':...</td>
    </tr>
    <tr>
      <th>172</th>
      <td>RWXDszIahx0ssqRKePG8Sv8eV</td>
      <td>tWaivYPxI2xAKQbaemD2Z0geV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 2900, 'currency'...</td>
    </tr>
    <tr>
      <th>183</th>
      <td>vFRoKcYPfTEvfchdCok6tR1eV</td>
      <td>pw6HNSAC1JNze6yNqs1hMh1eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 525, 'currency':...</td>
    </tr>
    <tr>
      <th>190</th>
      <td>VwlSj53jIe8tBokR16ol1wyeV</td>
      <td>f1LTsYbYpp0FxFqhVPWcc86eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 22620, 'currency...</td>
    </tr>
    <tr>
      <th>279</th>
      <td>tkV8tVYhoszOW6ugT4JwsveeV</td>
      <td>bRitLqDzdOK6tmlgvBxjxQxeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 1120, 'currency'...</td>
    </tr>
    <tr>
      <th>324</th>
      <td>7dW4X4DgBgYXCX9RmRzXHp3eV</td>
      <td>Rko4KusBhTF4ZiMOqJRAm4xeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 12008, 'currency...</td>
    </tr>
    <tr>
      <th>326</th>
      <td>PnkT35BCCoVTbPiajkjrQJneV</td>
      <td>1yUZ5z049fAOr776iuWFYAneV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 390, 'currency':...</td>
    </tr>
    <tr>
      <th>428</th>
      <td>lsTyY8KYvkmP8VblxwrZrhfeV</td>
      <td>JetjGSCTcGTDbFUOmlXJhTgeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 160, 'currency':...</td>
    </tr>
    <tr>
      <th>435</th>
      <td>pEwJ5hiRFYwLIvKdOsTvp8yeV</td>
      <td>ZgYG6jdV3KAHPwuYjlnaQV4eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 75, 'currency': ...</td>
    </tr>
    <tr>
      <th>486</th>
      <td>zZEvfWQ4DGw1I0IlbxJe9pneV</td>
      <td>tArMDhKQGTWsHng7YbUpvfqeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 375, 'currency':...</td>
    </tr>
    <tr>
      <th>490</th>
      <td>xqL6vNuxij5XB9bnVhX5fjleV</td>
      <td>9wVnPptyX0yrHjwUldiMVI8eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 270, 'currency':...</td>
    </tr>
    <tr>
      <th>556</th>
      <td>bVknMMXrJzHKMajvCyi7ecmeV</td>
      <td>3pPTwa6A4jWiR3gOSV97AigeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 330, 'currency':...</td>
    </tr>
    <tr>
      <th>579</th>
      <td>bNABXjfs1z5pDOzaun6UFvkeV</td>
      <td>5SvjHz5tIONAICdjlahCorqeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 60, 'currency': ...</td>
    </tr>
    <tr>
      <th>594</th>
      <td>ff4JDp1boxrmkhfiaQC6m1ieV</td>
      <td>zNi1PDBgmdT7YqFg37uk2gqeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 3987, 'currency'...</td>
    </tr>
    <tr>
      <th>603</th>
      <td>lM5b1vSgRFF7aXwKMj3zizoeV</td>
      <td>NAxB8W5GDxHUfCAPOgGyls0eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 190, 'currency':...</td>
    </tr>
    <tr>
      <th>637</th>
      <td>rNQ3lrHDe3TQaxeuEoYOfwzeV</td>
      <td>h8YmjGxZx1F2VFCAeu35BCxeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 680, 'currency':...</td>
    </tr>
    <tr>
      <th>685</th>
      <td>NGAVTiNs3cX0G82erdbJChAfV</td>
      <td>jbzg1myJ1xiuVi1VMKOjIB0eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 4000, 'currency'...</td>
    </tr>
    <tr>
      <th>714</th>
      <td>dwdX3PCf6Miwi5jDLulRCg8eV</td>
      <td>VC4b5HXEODeQZz7KGxVSulweV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 640, 'currency':...</td>
    </tr>
    <tr>
      <th>724</th>
      <td>FAtAlcMllmICTkRxDMGL94geV</td>
      <td>D7vA6TJRpqiARiqDuM5ad42eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 15, 'currency': ...</td>
    </tr>
    <tr>
      <th>732</th>
      <td>9AxDGqqHzLjzUacqbc9aatteV</td>
      <td>lye8DwGb7fmHIi1Z1FPTPK4eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 20, 'currency': ...</td>
    </tr>
    <tr>
      <th>738</th>
      <td>ByLivdiIxdiQKtTSkDphUdneV</td>
      <td>3PaFdrOWjc2YSYcCjCgFEEieV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 500, 'currency':...</td>
    </tr>
    <tr>
      <th>750</th>
      <td>dE3vFARqTwDbMkyhj2A5oMneV</td>
      <td>nnmxCIxCpM1UMmvQNAHKc8meV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 240, 'currency':...</td>
    </tr>
    <tr>
      <th>755</th>
      <td>dKaB2yQUemGUi0DZa5gufnieV</td>
      <td>7ZgqVorbsCM3NssKmLOOMQjeV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 100, 'currency':...</td>
    </tr>
    <tr>
      <th>902</th>
      <td>BmNUiLU5FVt55BMCS3jkyA7eV</td>
      <td>9EDXAeJcZuf61MQNadOEfD6eV</td>
      <td>None</td>
      <td>[{'applied_money': {'amount': 720, 'currency':...</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_returns[df_returns['return_tips'].notnull()]['return_tips'].to_json('nhat_meeting_Nov,01,2023/returns[return_tips].json')
```


```python
temp = df_returns.explode('return_tips').reset_index(drop=True)
temp.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>order_id</th>
      <th>source_order_id</th>
      <th>uid</th>
      <th>return_tips</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Fx2yaaYpL9t1ilC0jAEGWpneV</td>
      <td>pkNrlE2WIUTSUAMpW55g3FMtsuXZY</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>1</th>
      <td>FNEQFe34LezRbQY8fseoqEheV</td>
      <td>ZIrNqjgBccSPVSpsIgHJ3CqME4YZY</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>2</th>
      <td>LaxOSqaYms5meggAaP2GvVreV</td>
      <td>Tdh4vEhPkG7XnjUpob9m7VvQatLZY</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>3</th>
      <td>j9FC2AfO2PiApqFhgQFugAW58b7YY</td>
      <td>zvyS0sgV7xG3P9iSy2jWaMZFpsFZY</td>
      <td>rJ094B1vfbb7VXIKHdiFUD</td>
      <td>None</td>
    </tr>
    <tr>
      <th>4</th>
      <td>6JetLDPnYZkv0sRbM2tyBNxeV</td>
      <td>jfqocGwcOvW2fTr3FGLmfcUI8TWZY</td>
      <td>None</td>
      <td>None</td>
    </tr>
  </tbody>
</table>
</div>




```python
temp[temp['return_tips'].notnull()]['return_tips']
```




    63     {'applied_money': {'amount': 1920, 'currency':...
    161    {'applied_money': {'amount': 660, 'currency': ...
    172    {'applied_money': {'amount': 2900, 'currency':...
    183    {'applied_money': {'amount': 525, 'currency': ...
    190    {'applied_money': {'amount': 22620, 'currency'...
    279    {'applied_money': {'amount': 1120, 'currency':...
    324    {'applied_money': {'amount': 12008, 'currency'...
    326    {'applied_money': {'amount': 390, 'currency': ...
    428    {'applied_money': {'amount': 160, 'currency': ...
    435    {'applied_money': {'amount': 75, 'currency': '...
    486    {'applied_money': {'amount': 375, 'currency': ...
    490    {'applied_money': {'amount': 270, 'currency': ...
    556    {'applied_money': {'amount': 330, 'currency': ...
    579    {'applied_money': {'amount': 60, 'currency': '...
    594    {'applied_money': {'amount': 3987, 'currency':...
    603    {'applied_money': {'amount': 190, 'currency': ...
    637    {'applied_money': {'amount': 680, 'currency': ...
    685    {'applied_money': {'amount': 4000, 'currency':...
    714    {'applied_money': {'amount': 640, 'currency': ...
    724    {'applied_money': {'amount': 15, 'currency': '...
    732    {'applied_money': {'amount': 20, 'currency': '...
    738    {'applied_money': {'amount': 500, 'currency': ...
    750    {'applied_money': {'amount': 240, 'currency': ...
    755    {'applied_money': {'amount': 100, 'currency': ...
    902    {'applied_money': {'amount': 720, 'currency': ...
    Name: return_tips, dtype: object




```python
def extract_json(df, target_col, id_col, tid_name):
    filtered_df = df[df[target_col].notna()][[target_col, id_col]]
    explode_df = filtered_df.explode(target_col).reset_index(drop=True)
    explode_df = explode_df.rename(columns={id_col: tid_name})
    final_df = pd.json_normalize(explode_df[target_col])
    # lineItem_df = lineItem_df.rename(columns={'id': 'refund_id'})
    final_df[tid_name] = explode_df[tid_name].values

    cols = final_df.columns.tolist()
    cols = [cols[-1]] + cols[:-1]
    final_df = final_df[cols]
    # final_df.columns = final_df.columns.str.replace('.', '_')
    
    return final_df
```

#### EXPLORING DF_LINEITEM


```python
df_lineItem.columns
```




    Index(['order_id', 'uid', 'catalog_object_id', 'catalog_version', 'quantity',
           'name', 'variation_name', 'item_type', 'base_price_money.amount',
           'base_price_money.currency', 'gross_sales_money.amount',
           'gross_sales_money.currency', 'total_tax_money.amount',
           'total_tax_money.currency', 'total_discount_money.amount',
           'total_discount_money.currency', 'total_money.amount',
           'total_money.currency', 'variation_total_price_money.amount',
           'variation_total_price_money.currency',
           'total_service_charge_money.amount',
           'total_service_charge_money.currency', 'note', 'tare_quantity'],
          dtype='object')




```python
df_lineItem_september.columns
```




    Index(['order_id', 'uid', 'catalog_object_id', 'catalog_version', 'quantity',
           'name', 'variation_name', 'item_type', 'base_price_money.amount',
           'base_price_money.currency', 'gross_sales_money.amount',
           'gross_sales_money.currency', 'total_tax_money.amount',
           'total_tax_money.currency', 'total_discount_money.amount',
           'total_discount_money.currency', 'total_money.amount',
           'total_money.currency', 'variation_total_price_money.amount',
           'variation_total_price_money.currency',
           'total_service_charge_money.amount',
           'total_service_charge_money.currency', 'note'],
          dtype='object')




```python
df_lineItem.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 220257 entries, 0 to 220256
    Data columns (total 24 columns):
     #   Column                                Non-Null Count   Dtype  
    ---  ------                                --------------   -----  
     0   order_id                              220257 non-null  object 
     1   uid                                   220257 non-null  object 
     2   catalog_object_id                     217461 non-null  object 
     3   catalog_version                       217461 non-null  float64
     4   quantity                              220257 non-null  object 
     5   name                                  218927 non-null  object 
     6   variation_name                        217461 non-null  object 
     7   item_type                             220257 non-null  object 
     8   base_price_money.amount               220257 non-null  int64  
     9   base_price_money.currency             220257 non-null  object 
     10  gross_sales_money.amount              220257 non-null  int64  
     11  gross_sales_money.currency            220257 non-null  object 
     12  total_tax_money.amount                220257 non-null  int64  
     13  total_tax_money.currency              220257 non-null  object 
     14  total_discount_money.amount           220257 non-null  int64  
     15  total_discount_money.currency         220257 non-null  object 
     16  total_money.amount                    220257 non-null  int64  
     17  total_money.currency                  220257 non-null  object 
     18  variation_total_price_money.amount    220257 non-null  int64  
     19  variation_total_price_money.currency  220257 non-null  object 
     20  total_service_charge_money.amount     220256 non-null  float64
     21  total_service_charge_money.currency   220256 non-null  object 
     22  note                                  1808 non-null    object 
     23  tare_quantity                         2 non-null       object 
    dtypes: float64(2), int64(6), object(16)
    memory usage: 40.3+ MB



```python
df_lineItem[df_lineItem['tare_quantity'].notnull()]['tare_quantity']
```




    6610    
    7821    
    Name: tare_quantity, dtype: object



#### CONTINUING THE WORK


```python
parquet_list = ["Orders.parquet", "LineItem.parquet", "LineItemAppliedDiscounts.parquet", \
            "LineItemAppliedServiceCharges.parquet", "LineItemAppliedTaxes.parquet", \
            "Refund.parquet", "ReturnLineItem.parquet", "Returns.parquet"]
for parquet in parquet_list:
    directory_historic = "parquets_historical/"
    directory_since_september = "parquets_since_september/"
    directory_complete = "parquets_complete/"
    df_historic = pd.read_parquet(directory_historic + parquet)
    df_since_september = pd.read_parquet(directory_since_september + parquet)
    df_complete = pd.concat([df_historic, df_since_september])
    print("df_complete size before drop duplicates: ", df_complete.size)
    if df_historic.columns.equals(df_since_september.columns):
        print(f"{parquet} files (hist + sep) have the same columns")
    else:
        print(f"{parquet} files (hist + sep) DO NOT have the same columns")
        print("The column difference is as follows: ", set(df_historic.columns) ^ set(df_since_september.columns))
    
    df_complete = df_complete.drop_duplicates().reset_index(drop=True)
    
    print("df_complete size after drop duplicates: ", df_complete.size)
    df_complete.to_parquet(directory_complete + parquet, index=False)
    print("\n\n")
    
```

    df_complete size before drop duplicates:  2155986
    Orders.parquet files (hist + sep) have the same columns
    df_complete size after drop duplicates:  2155986
    
    
    
    df_complete size before drop duplicates:  5446104
    LineItem.parquet files (hist + sep) DO NOT have the same columns
    The column difference is as follows:  {'tare_quantity'}
    df_complete size after drop duplicates:  5446104
    
    
    
    df_complete size before drop duplicates:  45675
    LineItemAppliedDiscounts.parquet files (hist + sep) have the same columns
    df_complete size after drop duplicates:  45655
    
    
    
    df_complete size before drop duplicates:  0
    LineItemAppliedServiceCharges.parquet files (hist + sep) have the same columns
    df_complete size after drop duplicates:  0
    
    
    
    df_complete size before drop duplicates:  1007740
    LineItemAppliedTaxes.parquet files (hist + sep) have the same columns
    df_complete size after drop duplicates:  1007595
    
    
    
    df_complete size before drop duplicates:  8436
    Refund.parquet files (hist + sep) have the same columns
    df_complete size after drop duplicates:  8436
    
    
    
    df_complete size before drop duplicates:  26350
    ReturnLineItem.parquet files (hist + sep) DO NOT have the same columns
    The column difference is as follows:  {'return_modifiers'}



    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[31], line 18
         15     print(f"{parquet} files (hist + sep) DO NOT have the same columns")
         16     print("The column difference is as follows: ", set(df_historic.columns) ^ set(df_since_september.columns))
    ---> 18 df_complete = df_complete.drop_duplicates().reset_index(drop=True)
         20 print("df_complete size after drop duplicates: ", df_complete.size)
         21 df_complete.to_parquet(directory_complete + parquet, index=False)


    File ~/anaconda3/lib/python3.11/site-packages/pandas/util/_decorators.py:331, in deprecate_nonkeyword_arguments.<locals>.decorate.<locals>.wrapper(*args, **kwargs)
        325 if len(args) > num_allow_args:
        326     warnings.warn(
        327         msg.format(arguments=_format_argument_list(allow_args)),
        328         FutureWarning,
        329         stacklevel=find_stack_level(),
        330     )
    --> 331 return func(*args, **kwargs)


    File ~/anaconda3/lib/python3.11/site-packages/pandas/core/frame.py:6672, in DataFrame.drop_duplicates(self, subset, keep, inplace, ignore_index)
       6670 inplace = validate_bool_kwarg(inplace, "inplace")
       6671 ignore_index = validate_bool_kwarg(ignore_index, "ignore_index")
    -> 6672 duplicated = self.duplicated(subset, keep=keep)
       6674 result = self[-duplicated]
       6675 if ignore_index:


    File ~/anaconda3/lib/python3.11/site-packages/pandas/core/frame.py:6814, in DataFrame.duplicated(self, subset, keep)
       6812 else:
       6813     vals = (col.values for name, col in self.items() if name in subset)
    -> 6814     labels, shape = map(list, zip(*map(f, vals)))
       6816     ids = get_group_index(
       6817         labels,
       6818         # error: Argument 1 to "tuple" has incompatible type "List[_T]";
       (...)
       6822         xnull=False,
       6823     )
       6824     result = self._constructor_sliced(duplicated(ids, keep), index=self.index)


    File ~/anaconda3/lib/python3.11/site-packages/pandas/core/frame.py:6782, in DataFrame.duplicated.<locals>.f(vals)
       6781 def f(vals) -> tuple[np.ndarray, int]:
    -> 6782     labels, shape = algorithms.factorize(vals, size_hint=len(self))
       6783     return labels.astype("i8", copy=False), len(shape)


    File ~/anaconda3/lib/python3.11/site-packages/pandas/core/algorithms.py:822, in factorize(values, sort, na_sentinel, use_na_sentinel, size_hint)
        819             # Don't modify (potentially user-provided) array
        820             values = np.where(null_mask, na_value, values)
    --> 822     codes, uniques = factorize_array(
        823         values,
        824         na_sentinel=na_sentinel_arg,
        825         size_hint=size_hint,
        826     )
        828 if sort and len(uniques) > 0:
        829     if na_sentinel is None:
        830         # TODO: Can remove when na_sentinel=na_sentinel as in TODO above


    File ~/anaconda3/lib/python3.11/site-packages/pandas/core/algorithms.py:578, in factorize_array(values, na_sentinel, size_hint, na_value, mask)
        575 hash_klass, values = _get_hashtable_algo(values)
        577 table = hash_klass(size_hint or len(values))
    --> 578 uniques, codes = table.factorize(
        579     values,
        580     na_sentinel=na_sentinel,
        581     na_value=na_value,
        582     mask=mask,
        583     ignore_na=ignore_na,
        584 )
        586 # re-cast e.g. i8->dt64/td64, uint8->bool
        587 uniques = _reconstruct_data(uniques, original.dtype, original)


    File pandas/_libs/hashtable_class_helper.pxi:5943, in pandas._libs.hashtable.PyObjectHashTable.factorize()


    File pandas/_libs/hashtable_class_helper.pxi:5857, in pandas._libs.hashtable.PyObjectHashTable._unique()


    TypeError: unhashable type: 'numpy.ndarray'



```python

```
