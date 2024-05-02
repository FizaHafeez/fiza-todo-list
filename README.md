# fiza-todo-list
this is a todos list 
#! /usr/bin/env node

import inquirer from "inquirer"
let todos = [];
let condition = true;

while(condition) 
    {
        let todoQuestions = await inquirer.prompt(
        [
            {
                name: 'firstQuestion',
                type: 'input',
                message: "What would you like to add in your Todos?"
            },

            {
                name: 'sceondQuestion',
                type: 'confirm',
                message: "Would you like to add more in your todos?",
                default: "true"
                    
            }
        ]
    );
    todos.push(todoQuestions.firstQuestion);
    console.log(todos)
    // THE LOOP IS RUNNING ON THE BASED OF THIS VARIBLE CONDITION
    condition = todoQuestions.sceondQuestion;
          
}
