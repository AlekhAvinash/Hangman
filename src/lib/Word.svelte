<script>
  export let istr = "";
  let chLt = {};
  let astr = istr.toLowerCase().split("");
  for(let i = 0; i<astr.length; i++){
    if(astr[i].match('[a-z]')){
      if(astr[i] in chLt){
        chLt[astr[i]].push(i);
      }
      else{
        chLt[astr[i]] = [i];
      }
    }
  }
  let ostr = ""
  for(let i = 0; i<astr.length; i++){
    if(astr[i].match('[a-z]')){
      ostr += "_ ";
    }
    else{
      ostr += astr[i];
    }
  }
  let out = ostr.toString();
</script>

<div>
  {out}
</div>