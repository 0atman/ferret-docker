Ferret compiles clojure to native code.

Usage:
docker run -v $(pwd -P):/code -it 0atman/ferret-docker example.clj

ferret-lang.org

# Tips

Use this alias to compile clojure without any dependencies! (except for docker)

```
$ alias fd="docker run -v $(pwd -P):/code -it 0atman/ferret-docker"
$ fd example.clj
11:58:46 info dir => ./
11:58:46 info file => example.clj
11:58:49 info compiled => ./example.cpp
11:58:49 info building => g++ -std=c++11 -x c++ example.cpp
```
