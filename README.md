# RaspberryPi
dht22.uf2 is the compiled file that should be copied to the raspberry picow as explained in the video below. 

Write to us for any modifications and customizations - our contact can be found in the youtube video linked below, or the website https://hoven.in

Youtube Explanation: https://youtu.be/zgtEQqa-_Lg

========self notes for future needs====================

    case REPEATING_TIMER_TICK: {

      if (tick_counter++ > 200) tick_counter = 1;

      if (0 == (tick_counter % 2)) {
        if (dht22.read_from_dht())
        {
          printf("{\"v\":true, \"t\":%0.1f, \"h\":%0.1f}\n", dht22.get_last_temperature(), dht22.get_last_humidity());
        }
        else printf("{\"v\":false, \"t\":0, \"h\":0}\n");
      }
    }

                             break;
