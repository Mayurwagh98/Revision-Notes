## Create a stopwatch having start-stop and Reset buttons
```
import React, { useState, useEffect, useRef } from "react";

function Stopwatch() {
  const [time, setTime] = useState(0);
  const [isActive, setIsActive] = useState(false);
  const intervalRef = useRef(null);

  useEffect(() => {
    return () => clearInterval(intervalRef.current);
  }, []);

  const handleStart = () => {
    setIsActive(true);
    intervalRef.current = setInterval(() => {
      setTime((time) => time + 1);
    }, 1000);
  };

  const handleStop = () => {
    setIsActive(false);
    clearInterval(intervalRef.current);
  };

  const handleReset = () => {
    setIsActive(false);
    clearInterval(intervalRef.current);
    setTime(0);
  };

  const formatTime = (time) => {
    const minutes = Math.floor(time / 60);
    const seconds = time % 60;
    return `${minutes.toString().padStart(2, "0")}:${seconds
      .toString()
      .padStart(2, "0")}`;
  };

  return (
    <div>
      <div>{formatTime(time)}</div>
      <button onClick={handleStart} disabled={isActive}>
        Start
      </button>
      <button onClick={handleStop} disabled={!isActive}>
        Stop
      </button>
      <button onClick={handleReset}>Reset</button>
    </div>
  );
}

export default Stopwatch;
```
