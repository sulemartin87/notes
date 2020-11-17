[typescript deepdive](https://www.youtube.com/redirect?q=https%3A%2F%2Fgithub.com%2Fbasarat%2Ftypescript-book&event=video_description&redir_token=QUFFLUhqbktzY1RUTHlMYVd5ZjdneGgwSU0waDhPWG1pQXxBQ3Jtc0tudUl4SDl3ODZNYkV5YmJ3VWdMTVUtb0d2emtZeTFFSzY5NXRRR2ZRQ1hXSkJHZVBBWVVnbldpM3FBbHFLZzJMY0UwSzhETVZrSk9WMzM4Tjhuc1dlNVFfOF95ZDI3ZHF1LW12M0xSY2lsSktmQnV5WQ%3D%3D&v=ahCwqrYpIuM)

great tooling

catch bugs quicker

tsc index.ts to transpile

will transpile to es3 

create a tsconfig.json

compliler options 
have a target like es3 / es6 /esnext 
watch: true to save each time 
lib  for typing for certain classes
have integrated errors and docs

install @types/lodash community kept autocomplete and intellisense maintained by 3rd parties

type annotations 

implicit like let lucky = 23; //will assume is a number 
// add :any to assing to anything 

if we don't give a value it's assumed to be any anytype

variables are assigned like 

let lucky: any = 23;
can put 

let decimal: number = 6;
let hex: number = 0xf00d;
let binary: number = 0b1010;
let octal: number = 0o744;
let big: bigint = 100n;

let isDone: boolean = false;

let color: string = "blue";

let list: number[] = [1, 2, 3]; //array 

let list: Array<number> = [1, 2, 3]; //another array specifying a type 

if you know the value don't bother adding a type to it


you can create a new style;

type Style = 'bold' | 'italic' | 23;


interface sets types 

like 

interface Person {
    first: string;
    last: string;
    [key: string]: any //add any type you want after this and only the first 2 will be required
}

annnotate types to functions to enforce types

function pow(x: number, y: number): string //return type 

array = 
const arr: number[] = [] // to specify that it only has numbers 

tuples = array with a fixed length 

[number, string, boolean?] //add question mark to make it optional 

you can use the tuple to make params that are optional 
