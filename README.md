tojson is a tiny (127 sloc), header only library to convert xml and yaml documents into nlohmann::json objects.

### minimal functioning example

```c++
#include <iostream>
#include "tojson.hpp"

int main()
{
	using namespace tojson;

	json a = loadxml("./example.xml");
	json b = loadyaml("./example.yml");

	std::cout << a.dump(1) << std::endl;
	std::cout << b.dump(1) << std::endl;

	return 0;
}
```

### dependencies

- rapidxml
- yaml-cpp
- nlohmann::json
