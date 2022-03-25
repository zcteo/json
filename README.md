# JSON for Modern C++ Wrapper

Wrapper for [JSON for Modern C++](https://github.com/nlohmann/json)

```cpp
using json = nlohmann::json;

struct Foo
{
    std::string name;
    int age;
    JSON_DEFINE_INTRUSIVE_MAP(Foo, NAME, name, AGE, age);
};

int main()
{
    Foo foo{"ZhangSan", 20};
    json j = foo;
    std::cout << j.dump(2) << std::endl;
    return 0;
}
```

output

```json
{
  "AGE": 20,
  "NAME": "ZhangSan"
}
```