\define listeBacklink() [[$(titre)$]backlinks[]] -Index
\define existeBacklink() [[$(titre)$]backlinks[]]first[]]
\define existeComment() [field:commente[$(titre)$]]

<$list filter="[is[current]!field:pdp[non]]">

<$vars titre={{!!title}}>
<$list filter=<<existeBacklink>>> 
<div class="bbtPdP"> Articles renvoyant ici : <$list filter=<<listeBacklink>>><$link>(<$view field="title"/>)</$link> </$list><$list filter=<<existeBacklink>>><br/></$list>
</div>
</$list>
</$vars>

</$list>