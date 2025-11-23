# Axios
api for axios.com breaking news site
# main
```cpp
#include "Axios.h"
#include <iostream>

int main() {
   Axios api;

    auto topics = api.get_topics().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    topics.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```

