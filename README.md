# Visual-Studio-GitHub-Copilot-Chat-Debugger-Aware

 ## GitHub Copilot �� IntelliSense �� IntelliCode �ĶԱ�
   
   - IntelliSense �� Visual Studio ���õ�һ�������ɹ��ܣ������ݵ�ǰ�������ṩ���顣 ���ཨ������������ơ��������ࡣ IntelliSense ���ض������Եģ�������һ�����޵ı�����ԡ�

   - IntelliCode �� Visual Studio ��һ����չ����ʹ�� AI ���ݴ�����е�ģʽ�ṩ�����ܵ����в�ȫ���ܡ� ����Խ�� IntelliSense��ͨ�������������˽ⳣ����������Ӧ���Ƽ����顣

   - GitHub Copilot/Chat �������� Visual Studio �� AI �����Ĵ��������չ����������ʽ�������Ӵ�Ĵ������ݼ����ṩ�����ĸ�֪�Ĵ��뽨�顢����Ƭ�Σ����������������� �������ڶ��ֱ�����ԣ��� IntelliCode �� IntelliSense ��ȣ����ṩ�˸��߼��İ�����

     ��Ȼ�����߶�ּ����߿�����Ա�Ĺ���Ч�ʣ��� GitHub Copilot ���������������ĵ�������ӱ�����������ṩ��׼ȷ����ضȸ��ߵĽ��顣


# Shortcuts
## Visual Studio Code

```
Zoom In:  Ctrl + -
Zoom Out: Ctrl + =
```

## GitHub Copilot

   - ��ݼ�

```
Trigger suggestion: Alt + \
Next suggestion:  Alt + ]
Prev suggestion:  Alt + [
Open GitHub Copilot: Ctrl + Enter
```

   ![Alt text](assets/shortcuts.png)

   ![Alt text](assets/The-Ultimate-Manual-to-GitHub-Copilot.png)

   - The Ultimate Manual to GitHub Copilot
   
      GitHub Copilot �ռ��ֲ�
      
      https://nira.com/github-copilot/

## `VSCode` ���� `GitHub Copilot` ����С����

   - Ŀ��

      - ���Զ����顢�����Բ������������

   - Can GitHub Copilot stop auto-suggesting, instead be triggered by a keystroke?
      
      GitHub Copilot ����ֹͣ (��������) �Զ����� ������ͨ���ֹ�����������
      
      https://stackoverflow.com/questions/71224911/can-github-copilot-stop-auto-suggesting-instead-be-triggered-by-a-keystroke

   1. ����  `enableAutoCompletions`
      - `VSCode preference`
         
         "github.copilot.editor.enableAutoCompletions": false`

   1. `Control + Enter`

      - ���ұ� `GitHub Copilot` ���鴰���˹� 10 ѡ 1������ʹ��

      - �ÿ�ݼ��� `ipynb notebook` ��Ч����ͻ��`notebook` ����ִ�д��� `cell`

         - ���а����Ϊ Control + Shift + Alt+ Enter ���� �� `ipynb notebook` �ĵ��ñ�Ŀ�ݼ�

           https://github.com/orgs/community/discussions/7255

   1. `Alt + \`
      - Ȼ��������ݼ�����Ч


   ## `Visual Studio` `GitHub Copilot` invent by `GitHub` + `GitHub Copilot Chat` invent by `Microsoft`

   - GitHub Copilot Chat `ask copilot` �����Ĳ˵������֣�
     - ��װ˳�򣬵��� ����/���� �������

   - �ֱ����� output ����

   ## Visual Studio + proxy/fiddler/mitmweb + GitHub Copilot
   
   - accept non-trusted certificates automatically = true

      https://github.com/orgs/community/discussions/50484

   ## Visual Studio + debugging/debugger-aware + AskCopilot (GitHub Copilot Chat)

   https://devblogs.microsoft.com/visualstudio/simplified-code-refinement-and-debugging-with-github-copilot-chat/

   https://learn.microsoft.com/en-us/visualstudio/debugger/debug-with-copilot?view=vs-2022

   - debugger-aware

     - ��ʾ��
            
      ```csharp

      // ask/prompt:
      // ��ӵ�ǰ��ջ���жϣ�����c3�ͱ���c���ڵ�ǰ��ջ����ͬһ��������(failed)

      var c = new { a = 1, b = 2, c = 3 };

      var c1 = new { a = 1, b = 2, c = 3 };

      var c3 = c;

      ```

      ```csharp

      // ask/prompt:
      // base on current runtime frame, what's the new value of var a? (passed)

      // ������ʱ Debug -> Windows -> Locals ��ʱ�޸� a ��ֵ

      // Copilot Answer:
      // Based on the information provided in our previous conversation, the latest new value of a in the current runtime frame is 3. This is because a is initially assigned a value of 1, and then it is later assigned a new value of 3 by dividing 1 by b where b is assigned a value of 0. This division results in a runtime exception. 
      
      var a = 1;

      ```

   - ��̬����: �쳣��������

      ```csharp

      var b = 0;

      var a = 1 / b;
      
      ```

   - ��̬����: ���ܸ����������

      ����������

   -  �����ԱʼǱ�
    - Sql NoteBooks ���ݲ�ѯ��䷴������ 
      `create table` �� `insert`

      ```sql

      -- ��ʾ��
      -- generate table! and 10 rows random data one by one

      SELECT
        1 as f1
        , 'aaa' as f2
        , getdate() as f3
        , newid() as f4
        , N'aaa' as f5
        , 1.00 as f6
        , cast(1 as bit) as f7
      FROM
       a

      ```

# Visual Studio Code - Java Console Apps 
## Comments to code
1. Create new file - StockHelper.java
2. Add comment on top:  "A class to get stock (China Merchant Bank) open and close prices from SINA Finance" or "�����Ųƾ���ȡ�������й�Ʊ�Ŀ��̼ۺ����̼�"
3. Enter to get code 
4. or Ctrl + Enter to get code from suggestion list
5. Run Code
6. Fix the error with comment "//Add Referer header to the request to avoid 403 error"
7. Fix Charset error with code: Encoding.RegisterProvider(CodePagesEncodingProvider.Instance);
8. (Optional) Add new method with comments: 
   * Method to calculate days between two dates
   * Encrypt text using AES
   * Generate PDF file with iTextSharp
9. //Test method of XXX
