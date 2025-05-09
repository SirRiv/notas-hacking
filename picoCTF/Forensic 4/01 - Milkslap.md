## Descripción
[🥛](http://mercury.picoctf.net:29522/)
Hints:
1. Look at the problem category
## Solución 

```srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Milkslap$ export RUBY_THREAD_VM_STACK_SIZE=500000000
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Milkslap$ zsteg concat_v.png
imagedata           .. text: "\n\n\n\n\n\n\t\t"
b1,b,lsb,xy         .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"
b1,bgr,lsb,xy       .. /var/lib/gems/3.2.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect': stack level too deep (SystemStackError)
        from /var/lib/gems/3.2.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.2.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
        from /var/lib/gems/3.2.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.2.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
        from /var/lib/gems/3.2.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.2.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
        from /var/lib/gems/3.2.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.2.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
         ... 4807703 levels...
        from /var/lib/gems/3.2.0/gems/zsteg-0.2.13/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.2.0/gems/zsteg-0.2.13/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Milkslap$

```

~~~
picoCTF{imag3_m4n1pul4t10n_sl4p5}
~~~


## Notas adicionales 



## Referencias
