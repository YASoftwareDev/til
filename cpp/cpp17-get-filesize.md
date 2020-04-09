In C++17 there are `std::filesystem` file_size methods and functions, so that can streamline the whole task.

```cpp
    std::filesystem::file_size - cppreference.com
    std::filesystem::directory_entry::file_size - cppreference.com
```

With those functions/methods there's a chance not to open a file, but read cached data (especially with the `std::filesystem::directory_entry::file_size` method)

Those functions also require only directory read permissions and not file read permission (as `tellg()` does)

[Stackoverflow answer](https://stackoverflow.com/questions/22984956/tellg-function-give-wrong-size-of-file/54065421#54065421)

