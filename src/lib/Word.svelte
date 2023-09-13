<script>
  let chLt = {}
  let ostr = ""
  let astr = []


  export const update = (inp) => {
    if(inp in chLt)
      chLt[inp] = false
    else
      return false
    fill()
    checkWinner()
    return true
  }
  

  export const start = (inp) => {
    astr = inp.toLowerCase().split("")
    for(let i = 0; i<astr.length; i++)
      if(astr[i].match('[a-z]') && !(astr[i] in chLt))
        chLt[astr[i]] = true
    fill();
  }


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


  start("FIRE PALACE")
</script>

<div class="text-light d-flex justify-content-center fs-1 word">
  {ostr}
</div>

<style>
  .word{
    letter-spacing: 3px;
  }
</style>