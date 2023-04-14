# 1.18b compile-time errors

→ not including the # for pre-processor directives leads to the compiler trying to interpret as a type

→ forgetting std:: will tell you the thing you are trying to call is not in the scope

→ missing parenthesis will tell you exactly that