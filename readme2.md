cat in9.txt | grep -o "[0-9].*"

cat in10.txt | grep -o ".*\s[abc]\+"

cat in13b.txt | grep -o "J.*"
cat in13b.txt | grep -o "A.*"
cat in13b.txt | grep -o "\([A-Za-z]\+\s\([0-9]\+\)\s\).*\1"
cat in13b.txt | grep -o "\([A-Za-z]\+\s\)\([0-9]\)\+\s\1.*"

cat in15.txt | grep -o "[A-Z].*[ad].*"

Találja meg mindkét sort.
in16.txt 
The quick brown fox jumps over the lazy dog.
We had to censor the chat for saying &$#*@!. 
cat in16.txt | grep -o ".*"
cat in16.txt | grep -o "^[A-Z].\+\.$"

cat tortszamok.txt | grep -o ".*\..*"

cat in17.txt | grep -o "^\(+40\)\?\(0040\)\?1\?\s\?(\?\([0-9]\{3\}\))\?-\?\s\?\([0-9]\{3\}\))\?-\?\s\?\([0-9]\{3,4\}\)"

cat talaljamegazemaileket.txt | grep -o "\b[A-Za-z0-9.-]\+@[a-zA-z0-9.-]\+\b"
cat talaljamegazemaileket.txt | grep -o "\b[a-zA-Z0-9.*+-]\+@[a-zA-z0-9.-]\+\b"
cat talaljamegazemaileket.txt | grep -o "\b[a-zA-Z0-9._%+-]\+@[a-zA-z0-9.-]\+\b"


cat talaljamegazelso4sort.txt | grep -o "ftp.*\|https.*\|file.*\|http.*"
cat talaljamegazelso4sort.txt | grep -o "\(\w\+\)[^t]://.\+"



