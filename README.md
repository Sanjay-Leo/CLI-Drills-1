# CLI Drills 1
**Mountbluee CLI Drills 1**




* mkdir -p hello/{five/six/seven,one/two/three/four}
 
* touch hello/five/six/{c.txt,seven/error.log}
 
* touch hello/one/{a.txt,b.txt,two/{d.txt,three/{e.txt,four/access.log}}}
 
* tree
 
* find . -iname '*.log' -type f -delete
 
* open hello/one/a.txt
 
* rm -r hello/five
 
* mv hello/one/a.txt hello/one/two
 
* cd hello
 
* mv one uno
 
* tree






**At First the Directory structure looks like this** 

![1](https://user-images.githubusercontent.com/51887422/106748389-30120600-664b-11eb-91cd-ea9c2b256f11.JPG)


**After Deleting Log files & directory 5 & renaming it uno**

![Screen Shot 2021-02-03 at 6 07 19 PM](https://user-images.githubusercontent.com/51887422/106749155-2d63e080-664c-11eb-9727-a3de5ac7651e.JPG)




# CLI Drills 2


* curl -o voldemort.txt https://raw.githubusercontent.com/bobdeng/owlreader/master/ERead/assets/books/Harry%20Potter%20and%20the%20Goblet%20of%20Fire.txt

* head -n3 voldemort.txt

* tail -n10 voldemort.txt


**Word Occurance**

* grep -o -i 'harry' voldemort.txt | wc -l

* grep -o -i 'ron' voldemort.txt | wc -l

* grep -o -i 'hermione' voldemort.txt | wc -l

* grep -o -i 'Dumbledore' voldemort.txt | wc -l


* sed -n -e '100,200p' voldemort.txt

* tr ':;,?!\"' ' ' < voldemort.txt | tr -s ' ' '\n' | awk '!a[$0]++{c++} END{print c}'


**Process,Ports**

* pgrep Google Chrome          (9435,9447,9453, ...)

* echo $PPID                   (8962)

* kill <pid>
  
* ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem | head -n 3          (both memory & CPU usage)

* python -m http.server 8000


_(to stop process of local host)_

* sudo lsof -iTCP:8000 -sTCP:LISTEN      (after getting process-id PID)

* kill <pid>

* sudo python -m http.server 90          (port below 1024 require root privileges)

* sudo watch netstat -tulpn  sudo watch ss -tulpn

* sudo ss -lptn 'sport = :5432'


**Managing Software**       (for mac only not for linux)

* brew install htop

* brew install vim

* brew install nginx

* brew remove nginx

**MISC**

* curl ifconfig.me        (157.41.53.172)

* nslookup google.com     (172.217.26.174)

* ping -c 10 google.com  or  PING google.com

* brew search node           (for mac only not for linux)

* brew search code           (for mac only not for linux
 
 
