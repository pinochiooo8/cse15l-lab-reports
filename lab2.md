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

    @Override
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
    The output is shown below ![578c86c83669ce4fbf431e953c14281](https://github.com/pinochiooo8/cse15l-lab-reports/assets/121822382/fde62503-69f0-47a7-a2be-cec37878f451)

    
