# Xiangqi
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;

namespace wChess.ChessPieces
{
    /// <summary>
    /// 相
    /// </summary>
    public class Elephants:ChessPiece
    {
        public Elephants(Point metaPos, TEAM team = TEAM.RED, SIDE side = SIDE.UP)
            : base("象", metaPos, team,side)
        {
            if (Team == TEAM.BLACK)
                Name = "相";
        }
        public override List<Point> NextSteps
        {
            get 
            {
                List<Point> r = new List<Point>();
                //左上角预览
                if (FixedMetaPosition.X - 2 >= 0 && FixedMetaPosition.Y - 2 >= 0)
                {
                    //没有蹩相腰
                    if (ChessBoard.Matrix[FixedMetaPosition.Y - 1, FixedMetaPosition.X - 1] == 0)
                    {
                        var ps = ChessBoard.GetPieceFromMetaPos(FixedMetaPosition.X - 2, FixedMetaPosition.Y - 2);
                        //目标位置没有棋子；或者虽有棋子，但该旗子不是己方的
                        if (ps.Count == 0 || ps[0].Team != Team)
                        {
                            //相不能过河
                            if ((Side == SIDE.UP && FixedMetaPosition.Y - 2 < 5) || (Side == SIDE.DOWN && FixedMetaPosition.Y - 2 >= 5))
                            {
                                r.Add(new Point(FixedMetaPosition.X - 2, FixedMetaPosition.Y - 2));
                            }
                        }
                    }
                }

                //右上角预览
                if (FixedMetaPosition.X + 2 < ChessBoard.BOARD_META_WIDTH && FixedMetaPosition.Y - 2 >= 0)
                {
                    //没有蹩相腰
                    if (ChessBoard.Matrix[FixedMetaPosition.Y - 1, FixedMetaPosition.X + 1] == 0)
                    {
                        var ps = ChessBoard.GetPieceFromMetaPos(FixedMetaPosition.X + 2, FixedMetaPosition.Y - 2);
                        //目标位置没有棋子；或者虽有棋子，但该旗子不是己方的
                        if (ps.Count == 0 || ps[0].Team != Team)
                        {
                            //相不能过河
                            if ((Side == SIDE.UP && FixedMetaPosition.Y - 2 < 5) || (Side == SIDE.DOWN && FixedMetaPosition.Y - 2 >= 5))
                            {
                                r.Add(new Point(FixedMetaPosition.X + 2, FixedMetaPosition.Y - 2));
                            }
                        }
                    }
                }

                //右下角预览
                if (FixedMetaPosition.X + 2 < ChessBoard.BOARD_META_WIDTH && FixedMetaPosition.Y + 2 < ChessBoard.BOARD_META_HEIGHT)
                {
                    //没有蹩相腰
                    if (ChessBoard.Matrix[FixedMetaPosition.Y + 1, FixedMetaPosition.X + 1] == 0)
                    {
                        var ps = ChessBoard.GetPieceFromMetaPos(FixedMetaPosition.X + 2, FixedMetaPosition.Y + 2);
                        //目标位置没有棋子；或者虽有棋子，但该旗子不是己方的
                        if (ps.Count == 0 || ps[0].Team != Team)
                        {
                            //相不能过河
                            if ((Side == SIDE.UP && FixedMetaPosition.Y + 2 < 5) || (Side == SIDE.DOWN && FixedMetaPosition.Y + 2 >= 5))
                            {
                                r.Add(new Point(FixedMetaPosition.X + 2, FixedMetaPosition.Y + 2));
                            }
                        }
                    }
                }

                //左下角预览
                if (FixedMetaPosition.X - 2 >= 0 && FixedMetaPosition.Y + 2 < ChessBoard.BOARD_META_HEIGHT)
                {
                    //没有蹩相腰
                    if (ChessBoard.Matrix[FixedMetaPosition.Y + 1, FixedMetaPosition.X - 1] == 0)
                    {
                        var ps = ChessBoard.GetPieceFromMetaPos(FixedMetaPosition.X - 2, FixedMetaPosition.Y + 2);
                        //目标位置没有棋子；或者虽有棋子，但该旗子不是己方的
                        if (ps.Count == 0 || ps[0].Team != Team)
                        {
                            //相不能过河
                            if ((Side == SIDE.UP && FixedMetaPosition.Y + 2 < 5) || (Side == SIDE.DOWN && FixedMetaPosition.Y + 2 >= 5))
                            {
                                r.Add(new Point(FixedMetaPosition.X - 2, FixedMetaPosition.Y + 2));
                            }
                        }
                    }
                }
                return r;
            }
        }
    }
}
