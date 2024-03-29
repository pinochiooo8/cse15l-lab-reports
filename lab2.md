# Lab Report 2

## Part 1

The code of ChatServer is shown below

```
import java.io.IOException;
import java.net.URI;

public class ChatServer implements URLHandler {
    private StringBuilder chatHistory = new StringBuilder();
    public static void main(String[] args) throws IOException {
        int port = 8000; 
        ChatServer chatServer = new ChatServer();
        Server.start(port, chatServer);
    }
    public String handleRequest(URI url) {
        if ("/add-message".equals(url.getPath())) {
            String[] params = parseQuery(url.getQuery());
            String message = params[0];
            String user = params[1];

            chatHistory.append(user).append(": ").append(message).append("\n");
            return chatHistory.toString();
        }
        return "Invalid request";
    }  
    private String[] parseQuery(String query) {
        String[] params = new String[2]; 
        if (query != null) {
            String[] parts = query.split("&");
            params[0] = parts[0].substring(parts[0].indexOf('=') + 1);
            params[1] = parts[1].substring(parts[1].indexOf('=') + 1);
        }
        return params;
    }
}
```

a) For the input /add-message?s=Hello&user=jpolitz
    The output is shown below. 
    ![Image](578c86c83669ce4fbf431e953c14281.png)
The **Main, handleRequest, pareQuery** methods were called, for the **Main** method, *String[] args*  which is the command-line argument, and the relevant field *chatHistory* has no change. 
For the  **handleRequest** method, the relevant argument is *String query*, and the filed *chatHistory* changes when it's appending new messages, for this input, it changes to "jpolitz: Hello\n". 
For the **pareQuery** method, the relevant argument is *String query*, for this input the argument is "s=Hello&user=jpolitz". 

b) For the input /add-message?s=How are you&user=yash
    The output is shown below.
     ![Image](12c7431f5e47b71bef8f018790b2e19.png)
The **handleRequest, pareQuery** methods were called, for the **handleRequest** method, the relevant argument is *URI url*, which is ("/add-message?s=How are you&user=yash"), and the relevant field *chatHistory* changes from *"jpolitz: Hello\n"* to *"jpolitz: Hello\nyash: How are you\n"*.  
For the **pareQuery** method, the relevant argument is *String query*, for this input the argument is "s=How are you&user=yash". 

## Part 2 

The terminal interaction when I log into myieng6 account.
![Image](7dcb01adaed0eb016cdadad44968682.png)

The absolute path to the private key and public key  for my SSh key. 
![Image](b8c70fc5bdbc4b21ac96e60cbe8930f.png)
The id_rsa is the private key and the id_rsa.pub is the public key. 


## Part 3 


In week 2 or 3 of the lab, I learned about the setup and use of SSH (Secure Shell) keys. This included generating a key pair, understanding the difference between the private and public keys, and how to use them for secure, password-less authentication to remote servers. Additionally, I was introduced to essential Unix commands like mkdir for creating directories, and ssh and scp for securely accessing and transferring files between local and remote systems. 
