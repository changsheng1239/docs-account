---
title: Trial Balance not tally
description: A guide to Trial Balance not tally for SQL Account
slug: /faq/general-ledger/trial-balance-not-tally
tags: ["SQL Account", "FAQ", "General Ledger"]
---

If you trial balance is not tally, may try running the following check.

## Make sure Retained Earning must have 1 Account code

1. GL > Maintain Chart of Account

    ![1](../../../static/img/general-ledger/trial-balance-not-tally/1.png)

:::note
If your Retained Earning is empty, you may create under Reserve, then only drag into Retained Earning.
:::

## Make Sure Maintain Opening Is Tally

1. GL > Maintain Opening Balance

2. Untick Project at left top

3. Make sure Local DR and Local CR is tally. (Refer Pic2)

   ![2](../../../static/img/general-ledger/trial-balance-not-tally/2.png)

## Not tally due to current transaction

:::tip
If above 2 step is tally, which mean is current transaction cause not tally, kindly follow below step
:::

1. GL > Print Journal of Transaction Listing > Choose the date period which is not tally

2. Click on Preview

3. Select report name : GL Journal-of-Transaction-Imbalance-Document

4. The list show which mean is the document cause not tally.

5. May upload the backup file to us and mention the problem.
