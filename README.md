# Hesap Makinesi (Calculator) Project

## Overview

This Hesap Makinesi (Calculator) project was created as part of the Internet Computer Internship Bootcamp. It is an actor-based smart contract implemented in Motoko, the programming language for the Internet Computer platform.

## Features

### Variables
- `hucre`: An mutable integer variable representing the current value in the calculator.

### Functions

#### Toplama (Addition)
```
public func toplama(s: Int) : async Int {
  hucre += s;
  hucre
}
```
#### Cikarma (Subtraction)
```
Copy code
public func cikarma(s: Int) : async Int {
  hucre -= s;
  hucre
}
```
#### Carpma (Multiplication)
```
Copy code
public func carpma(s: Int) : async Int {
  hucre *= s;
  hucre
}
```
#### Bolme (Division)
```
Copy code
public func bolme(s: Int) : async ?Int {
  if (s == 0) {
    null
  } else {
    hucre /= s;
    ?hucre
  }
}
```
#### Temizle (Clear)

```
public func temizle() : async () {
  hucre := 0;
}
```

#### Usage
To use the Hesap Makinesi, you can create an instance of the hesap_makinesi actor and call its functions.

```
import hesap_makinesi "path/to/hesap_makinesi";

actor {
  let calculator = hesap_makinesi;

  // Perform calculations
  let result = await calculator.toplama(5);
  debug_show(result);  // Output: 5

  // Continue with other operations...
}
```
#### Notes
This project was developed for educational purposes during the Internet Computer Internship Bootcamp.
Author
Gürkan Sönmez

#### License
This project is licensed under the MIT License.


Feel free to modify and customize the README file according to your specific details and re
