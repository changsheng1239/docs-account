---
sidebar_position: 7
id: barcode
title: Barcode
description: A guide to setup Stock Barcode for SQL Account
slug: /barcode
tags: ["SQL Account", "Stock", "Barcode","Setup"]
---

# Step by Step : Report Design – GRN Barcode

1. Download GRN Barcode Report Template from below link :
    <br />1.1 Barcode Capture from Maintain Stock Item Barcode as Barcode <br />
    http://www.sql.com.my/webstore/templates/01-grn-barcode-20-40-captureitembarcode
    <br />1.2 Barcode Capture from Maintain Stock Item as Barcode <br />
    http://www.sql.com.my/webstore/templates/02-grn-barcode-35-25-captureitemcode

2. Step to Import the report to SQL
- Logon SQL | Tools | Report Designer | Click on Import | Fast Report(*.fr3) | Change to SQL Reports(*.rtm) | Select report download from Step1.1/Step 1.2 
<br />http://www.sql.com.my/sqlacc.intro/tutorial/ **Look for Step 10.01**

3. Purchase | Goods Received Note | Preview |

![1](/img/stock/barcode/1.png)

- Click on blue color link to enter into Report Design.

4. Change the Report type to MM due to Barcode size is small

![2](/img/stock/barcode/2.png)

5. Change barcode size - > File | Page Setup | Paper Size |

![3](/img/stock/barcode/3.png)

- Currently this sample is Width = 35mm | Height = 25mm

6. Click on SubRptNorm : Document_Detail

![4](/img/stock/barcode/4.png)

- **From here you may change the Barcode layout.**
7. Click on DBBarcode | Right click | Configure

![5](/img/stock/barcode/5.png)

7.1 : Type : Select 128 <br />
7.2 : Bar Width : This is barcode width

8. GRN Barcode Event
- View | Module | Click on Event Handlers | Procedure DetailBeforeDetail

![6](/img/stock/barcode/6.png)

This step is to capture Item Qty, if Qty 10, will repeat 10 Barcode label.


