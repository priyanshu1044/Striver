# Binary to Decimal Conversion

### Time Complexity : **O(n)**

### Space Complexity : **O(1)**

```cpp
int convert(int N, string &str)
{
    int ans = 0;
    int p2 = 1; // power of 2

    for (int i = str.size() - 1; i >= 0; i--) {
        if (str[i] == '1') {
            ans += p2;
        }
        p2 *= 2;
    }
    
    return ans;
}
```

# Decimal to Binary Conversion

### Time Complexity : **O(log n)**

### Space Complexity : **O(log n)**

```cpp
void toBinary(int n)
{
    // your code here
    string st="";
    while(n!=1){
        if(n%2==1){
            st+='1';
        }else{
            st+='0';
        }
        n=n/2;
    }
    for(int i=st.size();i>=0;i--){
        cout<<st[i];
    }
    return;
        
}
```

# 1's Complement

### Time Complexity : **O(n)**

### Space Complexity : **O(n)**

```cpp
void onesComplement(string &binary)
{
    for (int i = 0; i < binary.size(); i++) {
        if (binary[i] == '0') {
            binary[i] = '1';
        } else {
            binary[i] = '0';
        }
    }
}
```

# 2's Complement

### Time Complexity : **O(n)**

### Space Complexity : **O(n)**

```cpp
void twosComplement(string &binary)
{
    // 1's Complement
    for (int i = 0; i < binary.size(); i++) {
        if (binary[i] == '0') {
            binary[i] = '1';
        } else {
            binary[i] = '0';
        }
    }
    
    // Add 1 to get 2's complement
    int carry = 1;
    for (int i = binary.size() - 1; i >= 0; i--) {
        if (binary[i] == '1' && carry == 1) {
            binary[i] = '0';
        } else if (carry == 1) {
            binary[i] = '1';
            carry = 0;
        }
    }
}
```

# Bit Manipulation Operators

## AND Operator

### Time Complexity : **O(1)**

### Space Complexity : **O(1)**

```cpp
int bitwiseAnd(int a, int b)
{
    return a & b;
}
```

## OR Operator

### Time Complexity : **O(1)**

### Space Complexity : **O(1)**

```cpp
int bitwiseOr(int a, int b)
{
    return a | b; 
}
```

## XOR Operator

### Time Complexity : **O(1)**

### Space Complexity : **O(1)**

```cpp
int bitwiseXor(int a, int b)
{
    return a ^ b; 
}
```

## SHIFT Operators

### Time Complexity : **O(1)**

### Space Complexity : **O(1)**

```cpp
void bitShift(int n)
{
    int leftShift = n << 1;  // Left shift n by 1 (n * 2)
    int rightShift = n >> 1; // Right shift n by 1 (n / 2)
}
```

## NOT Operator

### Time Complexity : **O(1)**

### Space Complexity : **O(1)**

```cpp
int bitwiseNot(int n)
{
    return ~n;
}
```
# Swap Variable: using ( XOR )

### Time Complexity : **O(1)**

### Space Complexity : **O(1)**

```cpp
void swap(int &a, int &b)
{
    // a = 5 // b = 6
    a = a ^ b; // 5 ^ 6
    b = a ^ b; // 5 ^ 6 ^ 6 => b = 5
    a = a ^ b; // 5 ^ 6 ^ 5 => a = 6
}
```

check if ith bit is set or not

