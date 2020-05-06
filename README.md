LOVE22.EL
===========
Emacs script for writing in the style of Love 22

Michael D. Ernst <mernst@theory.lcs.mit.edu>

10/2/1990

last modified 10/18/1990


Description of love22.el
========================


 This file helps you write text in the style of Love 22, a peripatetic
 jester and perennial presidential candidate (on a platform of "FOOD",
 "CLOTH", and "RENTS") who looks exactly like Uncle Sam, and dresses the
 part.  He notices words such as "LOVE22" whose letters add up to 22 on
 the ABC chart.

```
    The ABC Chart
   A B C D E F G H I
   J K L M N O P Q R
   S T U V W X Y Z
   1 2 3 4 5 6 7 8 9
```

 In conversations, he points them out in real time, whether he's talking
 or listening, and in writing he emphasizes them with capitalization and
 quotation marks, sometimes substituting homonyms to make the addition
 work out.  This program lets you do the same, automatically.  The effect
 can be quite humorous in text -- some people mistake it for
 Zippification.  Try it on some text you have lying around to see the
 result.  (I have my mail-before-send-hook do this automatically on
 certain mail, depending on the recipient.)

 You can get $22 bills, a copy of Love 22's platform, and other fun stuff
 by sending a self-addressed stamped envelope (with a small donation, if
 you're feeling generous; I sent $2.22 last time) to
    Love 22
    PO Box 4022
    Key West, FL  33040

 The commands of interest are:
``` 
 show-abc-chart
    Displays the ABC chart in the *Help* buffer.
 abc-chart-word
    Reports the ABC chart value of the word at point.
    In Love22 mode, bound to C-x =.
 abc-chart-region
    Reports the ABC chart value of the current region.
    In Love22 mode, bound to M-=.
 love22-buffer
    Attempts to find words whose ABC chart values are 22 (or its multiples).
    Will group words together, substitute homonyms, look for roots of words,
    and try various other tricks.  The function 22-hook is called on each
    such word (or group of words) found; its default action is to upcase the
    word(s), surround it by quotes, and change spaces to hyphens if
    substitution (e.g. "2" for "too") occurred.
 love22-region
    Like love22-buffer; acts on the current region (between point and mark).
 love22-mode
    A minor mode to support writing of Love22 text.  Love22 mode causes the
    (almost) continual display of the ABC chart value value of the current
    word, as well as emphasizing words whose value is a multiple of 22, if 
    love22-emphasize is non-nil.  (This mode's emphasis functionality is
    considerably less than that of love22-buffer, but it operates in real
    time.)
```



See [this interview with Love 22](https://www.providencejournal.com/news/20190720/mark-patinkin-for-ris-love-22-life-is-quirky-numbers-game) for why you need this script