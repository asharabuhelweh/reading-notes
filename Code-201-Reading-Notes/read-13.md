# HTML5
HTML5 has proven a solution to many attempts to solve problems that occurred a long time ago Provide a standard API, implementation locally and consistently in multiple browsers, without having to rely on third-party plug-ins.

+ Web Storage: it was split out into its own specification and it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies and this data persists even when you close your browser.and From our JavaScript code, we’ll access HTML5 Storage through the localStorage object on the global window object and if we want to check for html5 storage we can use af unction called `supports_html5_storage()`


**USING HTML5 STORAGE**

the data is stored as a string and based on named key/value pairs then you can retrieve that data with the same key

+ you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets

There are also methods for removing the value for a given named key, and clearing the entire storage area

`interface Storage {`

  `deleter void removeItem(in DOMString key);`

 ` void clear();`
`};`

there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index

`interface Storage {`

 ` readonly attribute unsigned long length;`

  `getter DOMString key(in unsigned long index);`
`};`

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something.

**LIMITATIONS IN CURRENT BROWSERS**

“5 megabytes” which you’re storing strings, not data in its original format
“QUOTA_EXCEEDED_ERR” : when you exceed the limit of storage and until now no browser supports any mechanism for web developers to request more storage space.

**HTML5 STORAGE IN ACTION**

+ SQL is a standard language for accessing and manipulating databases

+ most of the action resides in the string you pass to the executeSql method. This string can be any supported SQL statement, including SELECT, UPDATE, INSERT, and DELETE statements. It’s just like backend database programming, except you’re doing it from JavaScript

+ there's alot of competing vision for advanced, persistent, local storage for web applications: the Indexed Database API, known as “IndexedDB.”

The API exposes what’s called an object store. An object store shares many concepts with a SQL database. There are “databases” with “records,” and each record has a set number of “fields.” Each field has a specific datatype, which is defined when the database is created. You can select a subset of records, then enumerate them with a “cursor.” Changes to the object store are handled within “transactions.”