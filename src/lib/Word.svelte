<script>
  export let istr = ""
  export const update = (inp) => {
    if(inp in chLt)
      chLt[inp] = false
    fill()
    checkWinner()
  }

  let chLt = {};
  
  let astr = istr.toLowerCase().split("");
  for(let i = 0; i<astr.length; i++)
    if(astr[i].match('[a-z]') && !(astr[i] in chLt))
      chLt[astr[i]] = true
  
  let ostr = "-"
  function fill(){
    ostr = ""
    for(let i = 0; i<astr.length; i++)
      if(astr[i].match('[a-z]') && chLt[astr[i]])
        ostr += "_";
      else
        ostr += astr[i];
  }

  function checkWinner(){
    let retr = true
    for(let i = 0; i<astr.length; i++)
      if(astr[i] in chLt)
        retr = !chLt[astr[i]] && retr
    if(retr)
      ostr = "Winner!"

  }
  fill();
</script>

<div class="text-light d-flex justify-content-center fs-1 word">
  {ostr}
</div>

<style>
  .word{
    letter-spacing: 3px;
  }
</style>