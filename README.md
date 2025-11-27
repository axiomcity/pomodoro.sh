# pomodoro.sh
a super pomodoro app for linux.
<img src="demo.png" width="600px">
# THE APP
[Source 📝](https://github.com/axiomcity/pomodoro.sh/blob/main/pomodoro.sh)

```bash

[[ ! $1 ]] && echo "Indiquer une durée : ./pomodoro.sh 5" && exit 0;
sec=$(($1*60));
ft_a ()

{
while [ $sec -gt 0 ]; do

        [[ $sec -le 3 ]] && ft_b;
        echo "PomOdoRo tiMe : $min ($sec sec)";
        sec=$(($sec-1));
        min=$(($sec/60));
        sleep .1;
        clear;
done
}

ft_b () 

{
        curl https://files.catbox.moe/zjjzkk.ogg -o dring.ogg;
        xdg-open dring.ogg;
        sleep ;
        ft_c;
}

ft_c()

{
        clear
        echo "On dirai que c'est terminé mec";
        echo "Recommencer le truc la ?";
        read -p "Durée du pomodoro min : " rsec && sec=$(($rsec*60)) && ft_a
        return 0;
        exit 0;
}

ft_a;


```
