---
sidebar_position: 1
id: report-fastreport-basicGuide
title: Basic Guide
description: Basic Guide to get start with Fast Report
slug: /faq/report/fastreport/basicGuide
tags: ["Fast Report", "Basic Guide"]
---

## Understand on Toolbar

1. **Report Object**

    ![1](../../../../static/img/report/fastReport-basicGuide/1.png)

2. **Align Toolbar**

    ![2](../../../../static/img/report/fastReport-basicGuide/2.png)

## Sales Inovice Bands

1. Understand on Bands

   1. Group Header
      - Grouping Header
      - To Print on every page, right click on ***Group Header Band***, select ***reprint on new page***

   2. Master Data
      - The ***Main*** Dataset of the report
      - Normally Bind to Main Dataset
      - Each Page allows to have 1 ***Main Dataset Only***

   3. Detail Data
      - To display ***all Item Details***

   4. Group Footer
      - Grouping Footer
      - Display on ***Last Page*** only

   5. Page Footer
      - Display on ***Every Pages***

2. Sample Layout in Design Mode

    ![3](../../../../static/img/report/fastReport-basicGuide/3.png)

3. Sample Layout on Preview Mode

    ![4](../../../../static/img/report/fastReport-basicGuide/4.png)

4. Print Position

   - Group Footer content will be printed at the pixel value input.
   - Higher Value = Higher Footer
   - without setting with print position, the group footer will be printed after the document
   detail records.
   - Example Source Code:

        ```pascal
        if Engine.FreeSpace < (GroupFooter1.Height + PageFooter1.Height + 30) then Engine.NewPage;

        Engine.CurY := Engine.PageHeight - GroupFooter1.Height - PageFooter1.Height - **60** ;
        ```

        :::info[note]
        **60** -> Higher Value = Higher Footer
        :::

   1. How to do the Print Position setting in Report?

      1. Click on ***Group Footer*** -> Click on ***Properties*** -> ***Events*** Tab -> Double Click on ***OnbeforePrint*** event name

            ![5](../../../../static/img/report/fastReport-basicGuide/5.png)

      2. Adjust the value

            ![6](../../../../static/img/report/fastReport-basicGuide/6.png)

5. Stop Position vs Print Count

    | Stop Position | Print Count |
    | :---:          |    :----:   |
    | Details will stop at the input value| Details will stop by number of records inputs|
    | Recommend    | Not recommend if using More Description        |
    | Value in Pixel    | Number of Records |

   1. How to do the Stop Position in Report?

      1. Right click ***DetailData1*** -> Click on ***Events*** Tab -> Double click ***onAfterCalcHeight*** name

            ![7](../../../../static/img/report/fastReport-basicGuide/7.png)

      2. Setting the stop position

            ![8](../../../../static/img/report/fastReport-basicGuide/8.png)

            :::tip[SMALL TIPS]
            1. Set Either Print Count or Stop Position
            2. use // to disable the command
            3. When you set both Print Count and Stop Position, system will capture Print Count.
            :::

      3. Sample on Print Position / Stop Position

            ![9](../../../../static/img/report/fastReport-basicGuide/9.png)

## How to design Simple Sales Invoice?

- Preview Invoice
- Click on Report Name to enter to Design Mode

1. **Add PICTURE**

   1. Click on Picture Object

        ![10](../../../../static/img/report/fastReport-basicGuide/10.png)

   2. Place on Report Page

        ![11](../../../../static/img/report/fastReport-basicGuide/11.png)

      - **Fix Picture**

         1. Click on Load

            ![12](../../../../static/img/report/fastReport-basicGuide/12.png)

         2. Select the Picture on your local drive

         3. Click on ![tick](../../../../static/img/report/fastReport-basicGuide/tick.png)

            ![13](../../../../static/img/report/fastReport-basicGuide/13.png)

         4. Adjust to the desire size

            ![14](../../../../static/img/report/fastReport-basicGuide/14.png)

      - **Capture Picture from Report Dataset**

            ![15](../../../../static/img/report/fastReport-basicGuide/15.png)

2. **Text Memo**

    **Add Customer Email Address**

      1. Click on Text Memo

            ![16](../../../../static/img/report/fastReport-basicGuide/16.png)

      2. Place on Report Page

      3. Enter Text : Email

            ![17](../../../../static/img/report/fastReport-basicGuide/17.png)

      4. Repeat Step i & ii

      5. Select Document_CompanyBranch -> Email Expression

            ![18](../../../../static/img/report/fastReport-basicGuide/18.png)

3. **Rich Text Object**

    **Add Note**

   1. Click on RichText Object

        ![19](../../../../static/img/report/fastReport-basicGuide/19.png)

   2. Place on Report Page

   3. Select Main -> Note

        ![20](../../../../static/img/report/fastReport-basicGuide/20.png)

4. **System Text**

    - **Add Sum Qty**

        1. Click on System Text Object

            ![21](../../../../static/img/report/fastReport-basicGuide/21.png)

        2. Place on the Report Page

        3. Select Aggregate value

            ![22](../../../../static/img/report/fastReport-basicGuide/22.png)

5. **Draw Line**

   1. Click on Line

      ![23](../../../../static/img/report/fastReport-basicGuide/23.png)

   2. Place on the Report Page

   3. Draw a line

      ![24](../../../../static/img/report/fastReport-basicGuide/24.png)

6. **Center Horizontally in Band**

   - Display the object in center horizontal

     1. Click on Object you want to show in center horizontal

     2. Click on Center Horizontally In Band

         ![25](../../../../static/img/report/fastReport-basicGuide/25.png)

7. **Align Left / Middle / Right**

   1. Click on the multiple Object to Align as same alignment. System will follow the first object as alignment

      ![26](../../../../static/img/report/fastReport-basicGuide/26.png)

8. **Save the File**

   1. File -> Save As -> Enter Report Name -> Save

   2. Preview and see the result

   Result:

   ![27](../../../../static/img/report/fastReport-basicGuide/27.png)

## How to create the Subreport in Report?

- Preview Invoice
- Click on ***Report Name*** to enter to Design Mode

   ![28](../../../../static/img/report/fastReport-basicGuide/28.png)

  1. Click on **Subreport Object**

      ![29](../../../../static/img/report/fastReport-basicGuide/29.png)

     1. Place on Report Page you want to show.

         ![30](../../../../static/img/report/fastReport-basicGuide/30.png)

  2. System will prompt a new blank page for Subreport

      ![31](../../../../static/img/report/fastReport-basicGuide/31.png)

  3. Click on **Insert Band** to design the layout or insert the data

      ![32](../../../../static/img/report/fastReport-basicGuide/32.png)

      *\*\*May refer 2.1 Understand Bands at Page 4 on what band to use*

## Check Box

1. **Simple CheckBox**

   1. Click on CheckBox object

      ![33](../../../../static/img/report/fastReport-basicGuide/33.png)

   2. Place on the place you want to show.

      ![34](../../../../static/img/report/fastReport-basicGuide/34.png)

   3. Press on the button

      ![35](../../../../static/img/report/fastReport-basicGuide/35.png)

   4. Select the frame design

      ![36](../../../../static/img/report/fastReport-basicGuide/36.png)

   5. Change to False

      ![37](../../../../static/img/report/fastReport-basicGuide/37.png)

   6. Save the File
      1. File -> Save As -> Enter Report Name -> Save
      2. Preview and see the result

   Result :

      ![38](../../../../static/img/report/fastReport-basicGuide/38.png)

2. **Query to show Check Box either True to False**

   1. Click on CheckBox | Double Click OnBeforePrint

        ![39](../../../../static/img/report/fastReport-basicGuide/39.png)

   2. Place a Query below

        ![40](../../../../static/img/report/fastReport-basicGuide/40.png)

        Query:

        ```pascal
        procedure Check/box1OnBeforePRint(Sender: TfrxComponent);
        begin
            if (Main."UDF_updated") = 'T' then
                checkbox1.checked := true
            else
                checkbox1.checked := false;
        end;
        ```

## How to do Report Watermark?

1. Insert Band | Select Overlay

   ![41](../../../../static/img/report/fastReport-basicGuide/41.png)

2. Insert Picture / Text to load in the water mark

   ![42](../../../../static/img/report/fastReport-basicGuide/42.png)

3. Overlay size can drag the same size as A4/Letter, and place the watermark on the position you want to show.

   ![43](../../../../static/img/report/fastReport-basicGuide/43.png)

4. File | Save As: Enter report name

5. Preview and see the Result :

   ![44](../../../../static/img/report/fastReport-basicGuide/44.png)

## Frequently Ask Question (FAQ)

### 1. Unit price is 0, display as FOC

In Memo, enter following syntax :

```pascal
[FormatFloat(',0.00;-,0.00;FOC ',<Document_Detail."UnitPrice">)]
```

![45](../../../../static/img/report/fastReport-basicGuide/45.png)

### 2. Document Currency Description change Cents to Sens

Syntax:

```pascal
[Document_Currency."Description"] : [StringReplace(CurrencyToLangWord(<Main."DocAmt">,<Profile."CurrencyLang">), 'CENTS', 'SENS', TRUE)]
```

![46](../../../../static/img/report/fastReport-basicGuide/46.png)

### 3. More Description convert RichTextToPlainText

Syntax :

```pascal
[RichTextToPlaintext(<Document_Detail."Description3">)]
```

![47](../../../../static/img/report/fastReport-basicGuide/47.png)

![48](../../../../static/img/report/fastReport-basicGuide/48.png)

### 4. How to change report paper size?

File -> Page Setting ->

![49](../../../../static/img/report/fastReport-basicGuide/49.png)

### 5. if Qty > 10, text color in red and in bold?

1. Double Click on Memo

2. Click on **Highlight Tab**

3. Click on **Add Button**

4. Expression value > 10

   ![50](../../../../static/img/report/fastReport-basicGuide/50.png)

5. Click on Font

   Can set for Font Type, Font Style, Size, Color or Effects

   ![51](../../../../static/img/report/fastReport-basicGuide/51.png)

6. Press **OK**

7. Right Click on Memo, **Ticked Allow Expression**

**Result** :

![52](../../../../static/img/report/fastReport-basicGuide/52.png)

### 6. Why in Report I have placed at the position I want, but when preview it will show at bottom?

Right click on Memo, **unticked Shift** and **Unticked Shift when Overlapped**

### 7. Export to PDF Logo is blur

![53](../../../../static/img/report/fastReport-basicGuide/53.png)

### 8. How to capture remark1 as url path?

In Memo properties :

Hyperlink Expression added in the Data Field Name

![54](../../../../static/img/report/fastReport-basicGuide/54.png)

Result :

![55](../../../../static/img/report/fastReport-basicGuide/55.png)

### 9. Payslip to show AL or MC Only

1. Click on **SubReport3**

2. Right click on **Leave MasterData Band**
   ![56](../../../../static/img/report/fastReport-basicGuide/56.png)

3. Click on Filter button

4. Enter the expression :

     ```pascal
     (<Leave."LeaveType"> ='AL') OR (<Leave."LeaveType"> ='MC')
     ```

5. Press OK

6. Press OK

   ![57](../../../../static/img/report/fastReport-basicGuide/57.png)

### 10. How to get Net Unit Price

 1. Click on **Memo Text**

 2. Place on **Document Detail Band**

 3. Drag data field from right to left box :

     ```pascal
     [<Document_Detail."Amount"> / <Document_Detail."Qty">]
     ```

 4. Press OK

 5. Adjust the position

 6. Preview and see the result

   ![58](../../../../static/img/report/fastReport-basicGuide/58.png)

### 11. UOM = UNIT, Qty display without Decimal Point, else with 2 Decimal Point

 1. Click On Memo Text

 2. Copy the below syntax and Paste into Memo:

     ```pascal
     [IIF(<Document_Detail."UOM"> = 'UNIT'>,
     FormatFloat('#,0;-#,0 ', <Document_Detail."Qty">) ,
     FormatFloat('#,0.00;-#,0.00 ', <Document_Detail."Qty">))]
     ```

    ![59](../../../../static/img/report/fastReport-basicGuide/59.png)

 3. Press **OK**

 4. Result After Preview :

    ![60](../../../../static/img/report/fastReport-basicGuide/60.png)

### 12. How to Get Supplier Bank in Payment Voucher?

 1. Click on Memo ![A](../../../../static/img/report/fastReport-basicGuide/A.png)

 2. Paste this syntax inside Memo

     ```pascal
     [<GetbankName(pl_SUPPLIERBANKACC."Bank">)]
     ```

    ![61](../../../../static/img/report/fastReport-basicGuide/61.png)

### 13. How to change the Amount in Word to First Character to Upper Case only?

Can use function NameCase

![62](../../../../static/img/report/fastReport-basicGuide/62.png)

Before :

![63](../../../../static/img/report/fastReport-basicGuide/63.png)

After :

![64](../../../../static/img/report/fastReport-basicGuide/64.png)
