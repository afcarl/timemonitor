Python Time Monitor
===================

Create several timers, increment them independently
and then print a summary.

Example:

    from time import sleep
    import timemonitor as tm
    with tm.TimeMonitor("sleep1"):
        print "Monitor sleep1"
        sleep(1)

    print "Exit from with stops the timer"

    print "Creating another monitor with the same name increments it again"
    with tm.TimeMonitor("sleep1"):
        print "Monitor sleep1"
        sleep(1)

    print "Second timer"
    with tm.TimeMonitor("sleep2"):
        print "Monitor sleep2"
        sleep(1)

    print tm.summarize() 
    Time Monitor
    sleep1     : 2.003 s
    sleep2     : 1.001 s
