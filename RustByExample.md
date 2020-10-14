# Rust By Example Note

* rustc
```
rustc src/main.rs
run ./main
```
* format
    * pretty print: {:#?}
    * impl fmt::Binary : {:b}
    * impl fmt::Display : multi write!()?;
    * 8 : format!("0o{:o}", foo)
    * 10 : format!("{}", foo)
    * 16 : format!("0x{:X}", foo)
* struct
    * three types : tuple/ C struct / field less
* variable
    * unused should be prefix with underscore (no warning)
    * shadow can to be different type
* From and Into
    * convert type a to type b
    * from : let x = XX::from(y);
    * into : let x: B = a.into();
* TryFrom and TryInto
    * convert type a to type b, return Result<T, Error>
* To and from String
    * to string : impl fmt::Display for A
    * from string : let a = “xx”.parse::<A>().unwrap();
* loop
    * label : can out target label loop
    * break with return value : break value;
* iter() vs iter_mut() vs into_iter()
    * iter : borrow
    * iter_mut : mut borrow
    * into_iter : move
* match
    * dereference *
    * Destruct &, ref, ref mut
    * @ bind value to name : Some(n @ 42) => {}
* if let
    * if Foo not implemented PartialEq
        * if Foo::Bar == a : error
        * if let Foo::Bar = a : ok