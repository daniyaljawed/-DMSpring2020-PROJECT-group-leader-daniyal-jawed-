#DM 103348: VEEN DIAGRAM WITH CONVERSTION OF INFIX TO POSTFIX #
###PROJECT MEMBERS###
StdID | Name
------------ | -------------
**63155** | **Daniyal jawed** 

## Project Description ##
A Venn diagram uses overlapping circles or other shapes to illustrate the logical relationships between two or more sets of items. Often, they serve to graphically organize things, highlighting how the items are similar and different.
my project is about how do we solve veen diagram and make it easy for you o sole them by using this project and how did you use veen diagram to convert infix to postfix and make the convertion east for everyone whom using this project.
oue aimed to deliver this project was that  many people faces difficulties to solve the problems of infix to postfix and it take ag quantity of our quality time so because of this project we can help to solve the problematic equations in few seconds of our quality time and save our time and strenth for other different important works.

##Discrete Math Concepts Used ##
In our project we uses the discrete math concept of  convertion by cnverting infix to post fix and also the concept of veen diagram and 
it is playing an role to make our project work because our porject based upon this concepts and without them its impossible to to solve the veen diagram. 
You may use more 3rd level heading to categorize this portion of the report as shown below.

###Example 1: infix to postfix###
```C#
class InfixToPostExpression
    {
        

        public string PostfixExpression(string infixExpression)
        {
            Stackno1 stack = new Stackno1(infixExpression.Length);
            int Length = infixExpression.Length;
            stack.Push('(');
            char[] Postfix = new char[Length];
            infixExpression += ')';
            int CountInfix = 0;
            int CountPostfix = 0;
            while (!stack.isEmpty())
            {
                char chacracter  = infixExpression[CountInfix++];
                if (chacracter  != '?' && chacracter  != '?' && chacracter  != '-' && chacracter  != '`' && chacracter  != '(' && chacracter  != ')')
                {
                    Postfix[CountPostfix++] = chacracter ;
                }
                else if (chacracter  == '(')
                {
                    stack.Push(chacracter );
                }
                else if (chacracter  == '?' || chacracter  == '?')
                {
                    while (true)
                    {
                        char item = stack.Pop();
                        if (item != '(')
                        {
                            Postfix[CountPostfix++] = item;
                        }
                        else
                        {
                            stack.Push(item);
                            break;
                        }
                    }
                    stack.Push(chacracter );
                }
                else if (chacracter  == '-')
                {
                    while (true)
                    {
                        char item = stack.Pop();
                        if (item == '-')
                        {
                            Postfix[CountPostfix++] = item;
                        }
                        else
                        {
                            stack.Push(item);
                            break;
                        }
                    }
                    stack.Push(chacracter );
                }
                else if (chacracter  == '`')
                {
                    while (true)
                    {
                        char item = stack.Pop();
                        if (item == '`')
                        {
                            Postfix[CountPostfix++] = item;
                        }
                        else
                        {
                            stack.Push(item);
                            break;
                        }
                    }
                    stack.Push(chacracter );
                }
                else if (chacracter  == ')')
                {
                    char item;
                    while ((item = stack.Pop()) != '(')
                    {
                        Postfix[CountPostfix++] = item;
                    }
                }

            }
            string dani = "";
            for (int i = 0; i < Postfix.Length; i++)
            {
                dani += Convert.ToString(Postfix[i]);
            }
            return dani;
        }
    }
```

##Problems Faced##
Replace this text with the explaination of the problems you faced in the project, and how you resolved them. Again you can give each of your problems a heading of level 3.

###Problem 1: I don't know how to Code for converion###
For this problem i have to contect my seniors and try to understand that how to code for this and also he gave me advice for this project regarding how to represnt everything in perfect order

###Problem 2: i was sick and i lost my group###
As you seen the title at the starting point we create a group for diffrent project but inthe mid times i get sick for 1 week or mor that why i cant get in touch with my group members and leader.
because of miss understanding thy think tht i might join some other group so they completed the project on github with out me and i have to make this project alone .

##References##
- GeeksforGeeks.
-  old project of oop and ds.
- code samples of senior person how help me.
- i used to get help in the project.
