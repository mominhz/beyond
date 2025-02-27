import React, { useState, useEffect } from "react";
import "./Tetrix.css";

const Tetrix = () => {
  const rows = 20;
  const cols = 10;
  const [board, setBoard] = useState(Array.from({ length: rows }, () => Array(cols).fill(0)));

  useEffect(() => {
    const interval = setInterval(() => {
      movePieceDown();
    }, 500);
    return () => clearInterval(interval);
  }, [board]);

  const movePieceDown = () => {
    setBoard((prevBoard) => {
      const newBoard = prevBoard.map((row) => [...row]);
      return newBoard;
    });
  };

  return (
    <div className="tetrix-container">
      <h1>Tetrix Game</h1>
      <div className="board">
        {board.map((row, rowIndex) => (
          <div key={rowIndex} className="row">
            {row.map((cell, colIndex) => (
              <div key={colIndex} className={cell ? "cell filled" : "cell"}></div>
            ))}
          </div>
        ))}
      </div>
    </div>
  );
};

export default Tetrix;
