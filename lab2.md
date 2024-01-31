# Lab Report 2

## Part 1

The code of ChatServer is shown below

```
import java.io.IOException;
import java.net.URI;
import java.util.HashMap;
import java.util.Map;

public class ChatServer implements URLHandler {

    private StringBuilder chatHistory = new StringBuilder();

    public static void main(String[] args) throws IOException {
        int port = 8001;
        ChatServer chatServer = new ChatServer();
        Server.start(port, chatServer);
    }

    @Override
    public String handleRequest(URI url) {
    if ("/add-message".equals(url.getPath())) {
        Map<String, String> queryPairs = parseQuery(url.getQuery());
        String user = queryPairs.getOrDefault("user", "Unknown");
        String message = queryPairs.getOrDefault("s", "");

        chatHistory.append(user).append(": ").append(message).append("\n");
        return "<pre>" + chatHistory.toString() + "</pre>";
    }

        return "Invalid request";
    }
    private Map<String, String> parseQuery(String query) {
        Map<String, String> queryPairs = new HashMap<>();
        if (query != null) {
            String[] pairs = query.split("&");
            for (String pair : pairs) {
                int idx = pair.indexOf("=");
                String key = idx > 0 ? pair.substring(0, idx) : pair;
                String value = idx > 0 && pair.length() > idx + 1 ? pair.substring(idx + 1)                  : null;
                queryPairs.put(key, value);
            }
        }
        return queryPairs;
    }
    
}
```
