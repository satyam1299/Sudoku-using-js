import React, { useState } from "react";

const start = [
  [   2, null,    5,    7, null, null, null, null, null],
  [null, null,    6, null, null, null,    1,    9,    5],
  [   7,    8, null, null, null, null, null,    6, null],
  [   8, null, null, null,    6, null, null, null,    3],
  [null,    4, null, null,    8, null,    3,    1, null],
  [null,    7, null, null,    2, null, null, null,    6],
  [null,    6, null, null, null, null,    2,    8, null],
  [null, null, null,    4,    1,    9, null, null, null],
  [null, null, null,    8, null, null,    9,    7, null],
]; //initially created board

function SudokuSolver() {
  const [board, setBoard] = useState(start);

  const handleChange = (r, c, data) => {
    const newBoard = [board];
    newBoard[r][c] = data; //inserting data to the particular location
    setBoard(newBoard);
  };

  return (
    <div className="board">
      {board.map((r, rIndex) => (
        <div className="r" key={rIndex}>
          {r.map((data, cIndex) => (
            <input type="number" min="1" max="9" data = {data || ""} onChange={(event) =>
                handleChange(rIndex, cIndex, Number(event.target.data))
              }
              key={`${rIndex}-${cIndex}`}
            />
          ))}
        </div>
      ))}
    </div>
  );
}

export default SudokuSolver;
