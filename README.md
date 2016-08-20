# [VB] ConsoleApp example
Sample code for console apps in Visual basic

    Sub Main()
        ' Startup info
        Console.ForegroundColor = ConsoleColor.Yellow 'Set color
        Console.WriteLine("Hello world")
        Console.ForegroundColor = ConsoleColor.White
        Commands()

    End Sub
    Sub Commands()
        ' Define commands list
        Dim response As String = Console.ReadLine
        If response = "/help" Or response = "/command 1" Or response = "/command 2" Or response = "/command 3" Or response = "/end" Then
            ' Run commands


            ' Help menu
            If response = "/help" Then
                Console.ForegroundColor = ConsoleColor.Gray
                Console.WriteLine("--- Help page 1/1 ---")
                Console.WriteLine("/command 1 -> Example command")
                Console.WriteLine("/command 2 -> Example command")
                Console.WriteLine("/command 3 -> Example command")
                Console.WriteLine("/end -> Exit")
                Console.ForegroundColor = ConsoleColor.White
                Commands()
            End If

            '######### Command 1
            If response = "/command 1" Then
                Console.WriteLine("Action 1!")
                ' You action here


                ' Back to menu
                Commands()
            End If
            '########## Command 2
            If response = "/command 2" Then
                Console.WriteLine("Action 2!")
                ' You action here


                ' Back to menu
                Commands()
            End If
            '########## Command 3
            If response = "/command 3" Then
                Console.WriteLine("Action 3!")
                ' You action here


                ' Back to menu
                Commands()
            End If
            If response = "/end" Then
                ' You action here
                End

                ' Back to menu
                ' -- No back ---
            End If
        Else
            ' Unkown command message
            Console.ForegroundColor = ConsoleColor.Red
            Console.WriteLine("Unkown command. Try /help for see list of commands")
            Console.ForegroundColor = ConsoleColor.White
            Commands()
        End If
    End Sub

