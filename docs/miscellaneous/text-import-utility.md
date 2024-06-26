---
sidebar_position: 16
id: text-import-utility
title: Text Import Utility Guide
description: A quick guide on Text Import Utility for SQL Account
slug: /miscellaneous/text-import-utility
tags: ["SQL Account", "Text", "Import"]
---

## Text Import Step

    1. Download [SQLAccXLSnMDBImp-setup.exe](https://download.sql.com.my/customer/Fairy/SQLAccXLSnMDBImp-setup.exe) in your pc.

    2. Run and Install the setup file.

    3. Log on to your correct database

        ![1](../../static/img/miscellaneous/text-import-utility/1.png)

    4. Double click the following icon

        ![2](../../static/img/miscellaneous/text-import-utility/2.png)

    5. Makesure the top is show the database you choose

        - Choose the transaction you want to import, eg. customer-maintain customer

            ![3](../../static/img/miscellaneous/text-import-utility/3.png)

    6. Open the patch file you save

        ![4](../../static/img/miscellaneous/text-import-utility/4.png)

    7. Invalid status...

        1. Go into SQL to add the status which are not in the database

            ![5](../../static/img/miscellaneous/text-import-utility/5.png)

        2. Example :

            ![6](../../static/img/miscellaneous/text-import-utility/6.png)

        3. So now, you go into your SQL, add the agent code

            ![7](../../static/img/miscellaneous/text-import-utility/7.png)

            ![8](../../static/img/miscellaneous/text-import-utility/8.png)

    8. Go back to the Text Import, **VERIFY** again.

        1. If the status show invalid again, go to the SQL and add in.

        2. After add in, get the file and verify again.

        3. For this example, go to Tools --> Maintain Area

            ![9](../../static/img/miscellaneous/text-import-utility/9.png)

        4. The status will shown **“** OK **”** once you complete.

            ![10](../../static/img/miscellaneous/text-import-utility/10.png)

        5. Once you post to A/C, go to SQL ...... Customer -–> Maintain Customer

        6. Log out and log in again, the new customer name will automatically shown in the customer list.

            ![11](../../static/img/miscellaneous/text-import-utility/11.png)
