Markdown + PHP + libupskirt
===========================

> Inspired by Rick Astley wearing a kilt

Upskirt is an implementation of John Gruber's Markdown markup
language. Upskirt is safe, fast and production ready. Check out
the original version at <http://git.instinctive.eu/cgit/libupskirt/>

Redcarpet is Upskirt with a touch of Ruby. It is mostly based on Ryan
Tomayko's RDiscount wrapper, and inspired by Rick Astley wearing a kilt.

Redcarpet is powered by a modified version of Upskirt, which has been
updated to pass the official Markdown test suite and now has support
for many additional features: autolinks, smartypants, safe filters,
and a long etcetera.

Redcarpet is a drop-in replacement for BlueCloth, RedCloth and RDiscount.

* Upskirt is (C)2009 Natacha PortÃ©
* Upskirt has been brought back to life and made standards-compilant in 2011 by Vicent Marti
* Redcarpet is (C)2011 Vicent Marti
* PHP_Redcarpet is (C)2011 Shuhei Tanuma
 

License
-------

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

Install
-------

php_redcarpet is just simple wrapper of <https://github.com/tanoku/redcarpet>.

    git clone https://github.com/chobie/php_redcarpet.git && cd php_redcarpet
    git clone https://github.com/tanoku/redcarpet.git
    mv config.m4  redcarpet/ext
    mv php_redcarpet.c redcarpet/ext
    mv php_redcarpet.h redcarpet/ext
    cd redcarpet/ext && phpize && ./configure
    make
		sudo make install
    # extension=redcarpet.so

Example
-------

    $markdown = new Redcarpet(string $text[, StdClass $extensions]);
    echo $markdown->to_html();