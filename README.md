# BashScript
for i in ` ps -ef | grep "airflow scheduler" | awk '{print $2}'`
do   
 echo $i
 sudo kill -9 $i
done


If you have to write it in single line
for i in ` ps -ef | grep "airflow scheduler" | awk '{print $2}’`;
do   
 echo $I;
 sudo kill -9 $I;
done

-ef (all and full description of processes)

* If any process automatically runs after getting killed, some crontab command is running behind most likely


* There is no by default support of named arguments.
It supports only positional arguments:
for ARGUMENT in "$@"
do

    KEY=$(echo $ARGUMENT | cut -f1 -d=)
    VALUE=$(echo $ARGUMENT | cut -f2 -d=)

    case "$KEY" in
            from)  from=${VALUE} ;;
            to)    to=${VALUE} ;;
            *)
    esac
done

echo "from = $from"
echo "to = $to"
