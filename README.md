# Chaitanyakrishna
###### Bawarchi 
Bawarchi restarent is famous for spicy biryani located hydrabad, **india near rtc cross roads** , and it is aslo located at very busy place , many theators , parks , hotals .**you will get the best food and services**sss. All types of indian spicy food is very famous 

# assignment2-chundiwar


--------------------------------------------------------------

# Kempigowda International  Airport
## kempigowda Airport is the closest Airport  located about 30 kilometres  suburb of Devanahalli ,Bengalore,India

   - The airport opened in May 2008 as an alternative to increased congestion at HAL Airport

   - take left to Devanahalli  so that you can enter into highway there are some Food restorant

   - Restorant name is  Barley & Grapes Cafe located 4 km to airport

   - there you will get some ice-creams  and good Snakes and fresh drinks

## Food items

1. Ice Creams
2. Fresh juices
3. Snakes 


[below is my image](https://github.com/chaitanya-chundiwar/assignment2-chundiwar/blob/main/AboutMe.md)
[link is above](https://github.com/chaitanya-chundiwar/assignment2-chundiwar/blob/main/AboutMe.md)




------------------------------------------------------------------------

# Sports

| Name   | Location   | Amount   |
|--------|------------|----------|
| BADMINTAN   | Nagpur   | $35   |
| Tennies   | Mumbai   | $25   |
| chess   | chennai   |$55   |

-------------------------------------------------------------------------


# Quotes

>"It's fine to celebrate success, but it is more important to heed the lessons of failure."

>"Intellectual property has the shelf life of a banana."

--------------------------------------------------------------------------


# code fencing

>What is String-Hashing? String hashing is the way to convert a string into an integer known as a hash of that string.An ideal hashing is the one in which there are minimum chances of collision (i.e 2 different strings having the same hash).

<https://www.geeksforgeeks.org/string-hashing-using-polynomial-rolling-hash-function/#:~:text=What%20is%20String%2DHashing%3F,strings%20having%20the%20same%20hash).>

```
int count_unique_substrings(string const& s) {
    int n = s.size();

    const int p = 31;
    const int m = 1e9 + 9;
    vector<long long> p_pow(n);
    p_pow[0] = 1;
    for (int i = 1; i < n; i++)
        p_pow[i] = (p_pow[i-1] * p) % m;

    vector<long long> h(n + 1, 0);
    for (int i = 0; i < n; i++)
        h[i+1] = (h[i] + (s[i] - 'a' + 1) * p_pow[i]) % m;

    int cnt = 0;
    for (int l = 1; l <= n; l++) {
        set<long long> hs;
        for (int i = 0; i <= n - l; i++) {
            long long cur_h = (h[i + l] + m - h[i]) % m;
            cur_h = (cur_h * p_pow[n-i-1]) % m;
            hs.insert(cur_h);
        }
        cnt += hs.size();
    }
    return cnt;
}
```

<https://cp-algorithms.com/string/string-hashing.html>

