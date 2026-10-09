<Html>
<Head>
<STYLE>

Body{

     font-family: arial;

	 font-size: 14;

	 color: darkblue;

	 }

table,td,tr,th{ 

     border-style: solid;

     border-width:1;

     border-collapse: collapse;

	 }

tr{

     background-color: lightgrey;

	 }

table{

     margin-left: 30%;

     margin-top: 10%;

     }	  
 
 
</STYLE>
</head>
<BODY>
<TABLE id=t1>
<TR><TH> Produkt </TH><TH> Preis </TH><TH> Menge </TH><TH></TH></TR>
<TR><TD> <Input id=i1 required > </Input></TD>
<TD> <Input id=i2> </Input></TD>
<TD> <Input id=i3> </Input></TD>
<TD> <Button id=b1> OK </Button></TD></TR>
</TABLE>
<BODY>
<SCRIPT>

let tab=document.getElementById('t1');

let b_ok=document.getElementById('b1');

let i_i1=document.getElementById('i1');

let i_i2=document.getElementById('i2');

let i_i3=document.getElementById('i3');
 
console.log(i_i1);
 
function eintragen(){

  let v_i1=i_i1.value;

  let v_i2=i_i2.value;

  let v_i3=i_i3.value;

  console.log(v_i1,v_i2,v_i3);

if(v_i1!='' )

{let tr=document.createElement('TR');

let td1=document.createElement('TD');

let td2=document.createElement('TD');

let td3=document.createElement('TD');
 
 
td1.innerText=v_i1;

td2.innerText=v_i2;

td3.innerHTML='Preis: '+v_i2+

               '<BR>Menge'+v_i3+

			   '<BR>Gesamtpreis' + Number(v_i2)*Number(v_i3);

tr.appendChild(td1);

tr.appendChild(td2);	

tr.appendChild(td3); tab.append(tr);
 
let b_del=document.createElement('Button')

b_del.style.backgroundColor='lightpink'

b_del.textContent='CLR';

tr.appendChild(b_del);

b_del.onclick=function(){tr.remove();i_i1.focus();}
 
} 

}

b_ok.onclick=function(){eintragen();}
 
 
</SCRIPT>
</Html>
 
