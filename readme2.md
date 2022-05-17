in9. cat in9.txt | grep -o "[0-9].*"
*Kiíratom azokat a sorokat, amelyek számokkal kezdődnek. utána pedig bármilyen karakter következhet.
 A 4. sor nem számmal kezdődik, ezért csak az első három sort fogom megkapni.*

in10. cat in10.txt | grep -o "^[0-9]\+\.\s\+[a-z]\+"

in13b./1. cat in13b.txt | grep -o "^\([A-Za-z]\{3\}\)\s\([0-9]\{4\}\)\s\2\s\([0-9]\{2\}\)\s\1\s\2"
in13b./2. cat in13b.txt | grep -o "^\([A-Za-z]\+\s\)\(2\(01\)1\)\s\1\3"

in15. cat in15.txt | grep -o -E ".*(cats$|dogs$)"

in16. cat in16.txt | grep -o "^[A-Z].\+\.$"

tört. cat tortszamok.txt | grep -o "^[0-9]\{3\}\?\,\?\-\?[0-9]*[.][0-9]\+\(\e-\)\?[0-9]\+$"

tel: cat in17.txt | grep -o "^\(+40\)\?\(0040\)\?1\?\s\?(\?\([0-9]\{3\}\))\?-\?\s\?\([0-9]\{3\}\))\?-\?\s\?\([0-9]\{3,4\}\)"

email: cat talaljamegazemaileket.txt | grep -o "^[A-Za-z0-9._%+-]\+@[A-Za-z0-9.-]\+"
*a /b jelentése még nem egyértelmű, adtam egy új megoldást nélküle.

linkek: cat talaljamegazelso4sort.txt | grep -o "^ftp.\+\|^https.\+\|^file.\+\|^http.*"
        cat talaljamegazelso4sort.txt | grep -E "^(ftp|http|https|file)"
        cat talaljamegazelso4sort.txt | grep -o "^\([a-z]\)\+://[a-z0-9_-]\+\(\.[a-z]\+\|:[0-9]\+\)\(/.*\)*"