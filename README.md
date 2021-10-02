# parenthesis-checker



class Solution
{
    public:
    //Function to check if brackets are balanced or not.
    bool ispar(string x)
    {
        int i = 0;
stack<char> st;
while(x[i] != '\0') {
if(!st.empty()) {
if(st.top() == '(' && x[i] == ')') st.pop();
else if(st.top() == '{' && x[i] == '}') st.pop();
else if(st.top() == '[' && x[i] == ']') st.pop();
else st.push(x[i]);
}
else {
st.push(x[i]);
}
i++;
}
return st.empty();
    }

};
