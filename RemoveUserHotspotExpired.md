:foreach a in=[/tool user-manager user find] do={:if ([/tool user-manager user get $a credit-left]=0s) do={

:log warning ("menghapus user $[/tool user-manager user get $a name] yang sudah expired..")
/tool user-manager user remove [/tool user-manager user get $a name]
}}

di schendule

sumber : http://www.forummikrotik.com/scripting-@-mikrotik/17584-%5Bshare%5D-script-delete-user-hotspot-yg-expired.html