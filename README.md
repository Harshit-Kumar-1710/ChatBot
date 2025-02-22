#include<iostream>
#include<unordered_map>
using namespace std;
int main()
{
    string UserInput;
    unordered_map<string,string>ChatBot;
    cout<<"ChatBot:Hello! Type 'bye' to exit.\n";
    ChatBot={{"hi","hello! how are you user"},{"i am fine.how about you?","i am doing great!!"},
        {"hello","what can i do for you?"},
        {"who are you?","i'm just a bot named aina and can answer to your queries anytime anywhere!"},
        {"what is your name","i'm just a personalised chatbot created in c++"},
        {"can i tell you anything to do?","no i'm just a basic chatbot.i'm in development mode.would be able to answer your queries in future"},
        {"bye","good bye have a great day!!"}};
    while(true)
    {
        cout<<"You: ";
        getline(cin,UserInput);
        for(char &c:UserInput)
        {
            c=tolower(c);
        }
        if(ChatBot.find(UserInput)!=ChatBot.end())
        {
            if(UserInput=="bye")
            {
                cout<<"ChatBot: "<<ChatBot[UserInput]<<endl;
                break;
            }
            else
            {
                cout<<"ChatBot: "<<ChatBot[UserInput]<<endl;
            }
        }
        else
        {
            cout<<"ChatBot: Sorry.I can't understand.\n";
        }
    }
return 0;
}
