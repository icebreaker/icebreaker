Mihail Szabolcs
===============
Senior Software Engineer, Open Source Evangelist, Renaissance Man.

- [mihail.co][1]
- [Twitter][2]

GitHub Contributions Snake
--------------------------
In order to play snake in the contributions matrix below, perform the following incantations:

1. create a bookmark with the code below
2. click on it while on this page
3. scroll down to the contributions matrix
4. use the arrow keys to control the snake

```javascrupt
javascript:(function(){class t{constructor(){this.reset(),window.addEventListener("keydown",this._onKeyDown)}reset=()=>{this.left=!1,this.right=!1,this.up=!1,this.down=!1};_onKeyDown=t=>{switch(t.preventDefault(),t.stopPropagation(),t.keyCode){case 37:this.left=!0;break;case 38:this.up=!0;break;case 39:this.right=!0;break;case 40:this.down=!0}}}const e="You can only play GitHub Contributions Snake on your GitHub profile!";class s{constructor(){let s=[],i=0,r=0;const a=document.querySelectorAll(".js-calendar-graph-svg g .ContributionCalendar-day");if(0<a.length){a.forEach(t=>t.setAttribute("data-level",0)),i=Math.ceil(a.length/7),r=7,s=Array(i*r).fill(-1);for(let e=0;e<r;e++)for(let t=0;t<i;t++)s[t+e*i]=a[e+t*r]}else document.querySelectorAll(".js-calendar-graph-table tr").forEach(t=>{let e=t.querySelectorAll(".ContributionCalendar-day");e.length>i&&(i=e.length),e.forEach(t=>{t.removeAttribute("tabindex"),t.setAttribute("data-level",0),s.push(t)}),r++});if(0==i||0==r)throw alert(e),e;this.tiles=s,this.w=i,this.h=r}set_tile_at=(t,e,s)=>{var{tiles:i,w:r}=this;let a=i[e+s*r];a&&-1!=a&&a.setAttribute("data-level",t)};get_tile_at=(t,e)=>{var{tiles:s,w:i}=this;let r=s[t+e*i];return r&&-1!=r?parseInt(r.getAttribute("data-level")):-1}}class i{constructor(t){this.grid=t,this.dx=1,this.dy=0,this.dt=0,this.tiles=[{x:2,y:3},{x:3,y:3},{x:4,y:3}],t.set_tile_at(2,5,5)}moveTo=(t,e)=>{this.dx=t,this.dy=e};draw=()=>{const{tiles:t,grid:e}=this;for(var s=0;s<t.length;s++){var i=t[s];e.set_tile_at(4,i.x,i.y)}};update=t=>{const{dx:e,dy:s,grid:i,tiles:r}=this;if(this.dt+=t,!(this.dt<.2)){this.dt=0;var a=(t=r[r.length-1]).x+e,l=t.y+s;if(!(a<0||a>i.w-1||l<0||l>i.h-1)&&-1!=(t=i.get_tile_at(a,l))&&4!=t)if(r.push({x:a,y:l}),t<=1){t=r.shift();i.set_tile_at(0,t.x,t.y)}else for(let t=0;t<7;t++){a=Math.floor(1+Math.random()*(i.w-1)),l=Math.floor(1+Math.random()*(i.h-1));if(0==i.get_tile_at(a,l)){i.set_tile_at(2,a,l);break}}}}}(new class{constructor(){this.keyboard=new t,this.grid=new s,this.snake=new i(this.grid)}run=()=>{this.last=0,this._tick(0)};_tick=t=>{const{keyboard:e,snake:s,last:i,_tick:r}=this;var a=.001*(t-i);this.last=t,e.left?s.moveTo(-1,0):e.right?s.moveTo(1,0):e.up?s.moveTo(0,-1):e.down&&s.moveTo(0,1),s.update(a),s.draw(),e.reset(),requestAnimationFrame(r)}}).run()})();
```

[1]: https://mihail.co
[2]: https://twitter.com/c0d3rguy
